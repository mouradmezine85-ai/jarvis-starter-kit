# /commit

> Commande pour sauvegarder l'état actuel du workspace dans Git, proprement, avec un message de commit clair.

---

## Mission

Quand je lance `/commit` (avec ou sans argument), exécute la séquence suivante.

**Si j'ai passé un argument** après la commande (exemple : `/commit refonte prix catalogue`), utilise-le comme indice pour rédiger le message, sans me reposer la question.

**Sinon**, pose-moi la question à l'étape 2.

---

### Étape 1 : Vérifier l'état du workspace

Lance `git status --short` pour voir ce qui a changé depuis le dernier commit.

Si rien n'a changé, dis-le simplement :

```
Rien à sauvegarder. Le workspace est déjà à jour avec le dernier commit.
```

Et arrête-toi là.

Sinon, continue.

---

### Étape 2 : Vérifier la sécurité avant tout

**ÉTAPE CRITIQUE, ne jamais sauter.**

1. Vérifie que `.env` n'apparaît PAS dans la liste des fichiers à committer :
   ```
   git ls-files --others --exclude-standard | Select-String "\.env$"
   git diff --cached --name-only | Select-String "\.env$"
   ```
2. Si `.env` apparaît quelque part, **ARRÊTE TOUT** et alerte :
   ```
   ALERTE SÉCURITÉ : le fichier .env est sur le point d'être commité.
   Vérifie le .gitignore avant de continuer. Je n'ai rien fait.
   ```
3. Scanne aussi les fichiers modifiés pour détecter des strings suspectes (clés API, tokens) qui auraient pu être copiées par erreur dans un fichier non protégé. Signale toute occurrence qui ressemble à :
   - `sk-...`, `pk_...`, `shpat_...`, `EAA...` (patterns de clés connus)
   - Chaînes de plus de 40 caractères qui ressemblent à des tokens

---

### Étape 3 : Résumer les changements

Présente-moi un résumé clair :

```
Voici ce qui a changé depuis le dernier commit :

**Nouveaux fichiers**
- [liste]

**Fichiers modifiés**
- [liste]

**Fichiers supprimés**
- [liste]
```

---

### Étape 4 : Proposer un message de commit

Rédige un message de commit **en français**, qui respecte ces règles :

- **Première ligne** : résumé court (max 72 caractères), à l'impératif ou au participe passé selon ce qui est le plus naturel. Pas de point final.
- **Ligne vide**, puis une description en bullet points si plusieurs changements importants.
- Pas de tirets longs (em dashes), uniquement des tirets simples ou des points.
- Pas d'emoji sauf si je le demande.
- Pas de co-author "Generated with Claude Code", pas de signature automatique.

Exemples de bons messages :

```
Ajout du dossier livrables et gestion des secrets

- Dossier livrables/ avec README et convention de nommage
- .env, .env.example et .gitignore pour les clés API
- Mise à jour du README et de CLAUDE.md
```

```
Mise à jour contexte Ets Mezine : budget marketing scenario A
```

Présente-moi le message proposé et demande :

```
Voici le message que je propose :

---
[message complet]
---

Je commit ? (oui / modifier / annuler)
```

---

### Étape 5 : Exécuter le commit

Si je valide :

1. Ajoute tous les fichiers tracés et les nouveaux fichiers non ignorés :
   ```
   git add .
   ```
2. Vérifie une dernière fois avec `git status --short` que `.env` n'est pas listé en `A` (added) ou `M` (modified staged).
3. Commit avec le message validé, en utilisant un here-string PowerShell pour supporter les retours à la ligne :
   ```powershell
   git commit -m @'
   [message]
   '@
   ```
4. Affiche le résultat avec `git log -1 --oneline`.

---

### Étape 6 : Confirmer

```
Sauvegardé. Commit [hash court] sur la branche [branche].

[git log -1 --oneline]
```

Si je demande à voir plus de détails, propose : `git log --oneline -10` pour l'historique récent.

---

## Règles importantes

- **Git n'est pas forcément dans le PATH** de PowerShell. Au début de chaque commande Git, ajoute Git au PATH de la session :
  ```powershell
  $env:Path = "C:\Program Files\Git\cmd;" + $env:Path
  ```
- **Ne commit jamais `.env`** ni aucun fichier contenant des secrets. En cas de doute, arrête et demande.
- **Ne push jamais sur un remote** sans que je te l'aie explicitement demandé. Cette commande fait uniquement un commit local.
- **Ne force jamais** (`--force`, `--amend` sur un commit déjà poussé, `reset --hard`) sans demander.
- Si le repo n'est pas encore initialisé (`git status` échoue), propose de lancer `git init` d'abord.
- Communication en français systématique, tutoiement.
- Pas de tirets longs dans les messages de commit.
