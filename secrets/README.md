# Gestion des secrets et clés API

> Comment stocker, utiliser et protéger mes clés API dans ce workspace.

---

## Les deux fichiers à connaître

À la racine du workspace, deux fichiers gèrent les secrets :

| Fichier | Rôle | Partageable ? |
|---------|------|---------------|
| `.env` | Mes vraies clés API | **Non, jamais** |
| `.env.example` | Modèle vide avec la liste des clés attendues | Oui |

Le fichier `.env` est protégé par `.gitignore`. Il reste uniquement sur mon ordinateur et n'est jamais envoyé sur Git/GitHub.

---

## Comment ajouter une nouvelle clé API

1. Ouvrir `.env` à la racine du workspace
2. Ajouter la ligne : `NOM_DE_LA_CLE=valeur-de-la-cle`
3. Ajouter aussi la même ligne (avec une valeur fictive) dans `.env.example` pour garder le modèle à jour
4. Sauvegarder

Convention de nommage : tout en MAJUSCULES avec des underscores. Exemple : `SHOPIFY_ADMIN_API_TOKEN`.

---

## Comment Claude lit mes clés

Quand Claude a besoin d'une clé (pour appeler une API Shopify, Meta, Google, etc.), il la lit dans `.env` au moment de l'exécution. Il ne la stocke pas et ne la mémorise pas entre les sessions.

Je peux aussi lui dire explicitement :
> "Prends ma clé Shopify dans `.env` et utilise-la pour..."

---

## Sécurité : les règles d'or

### À faire
- Garder `.env` uniquement sur mon ordinateur
- Révoquer immédiatement une clé si elle fuite (via le dashboard du service concerné)
- Faire tourner (régénérer) les clés tous les 6 à 12 mois pour les services sensibles
- Donner le minimum de permissions à chaque clé (ex: Shopify en lecture seule si pas besoin d'écrire)

### À ne jamais faire
- Commiter `.env` sur Git ou GitHub
- Copier-coller une clé dans un chat public, un email ou un screenshot
- Partager mon fichier `.env` par email, WhatsApp ou cloud public
- Mettre une clé en dur dans un script (toujours la lire depuis `.env`)

---

## Fichiers de credentials spéciaux (JSON, PEM, etc.)

Certains services (Google Cloud, Firebase, etc.) utilisent des fichiers de credentials au format JSON ou PEM au lieu d'une simple clé.

Convention : ranger ces fichiers dans le dossier `secrets/` à la racine. Ils sont déjà protégés par `.gitignore`.

Exemple :
```
secrets/
├── README.md                       # Ce fichier
├── google-service-account.json     # (exemple, ignoré par Git)
└── shopify-webhook.pem             # (exemple, ignoré par Git)
```

---

## Que faire en cas de fuite d'une clé

1. **Révoquer la clé immédiatement** sur le dashboard du service
2. **Générer une nouvelle clé** avec les mêmes permissions
3. **Mettre à jour `.env`** avec la nouvelle valeur
4. **Vérifier les logs** du service pour détecter un usage suspect
5. **Noter l'incident** dans `context/HISTORY.md` pour en garder la trace
