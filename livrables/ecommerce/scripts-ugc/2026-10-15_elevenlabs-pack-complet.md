# Pack complet ElevenLabs — Voix off Lilyeve en darija algéroise
## Guide pas à pas + textes optimisés + réglages exacts

> **Date :** 2026-10-15
> **Objectif :** Générer la voix off du script UGC Lilyeve en darija algéroise, qualité maquette, en moins de 15 minutes.
> **Coût estimé :** Gratuit (plan Free d'ElevenLabs = 10 000 caractères/mois offerts, nos 3 versions font ~2 500 caractères au total).

---

## ÉTAPE 1 — Créer ton compte ElevenLabs (3 minutes)

1. Va sur **https://elevenlabs.io**
2. Clique "Sign Up" en haut à droite
3. Inscris-toi avec ton Gmail (**mouradmezine85@gmail.com**) ou Google Login (le plus rapide)
4. Confirme l'email si demandé
5. Tu arrives sur le dashboard. En haut à droite, tu dois voir **"10 000 credits left"** ou similaire → c'est ton quota gratuit mensuel

**Pas besoin de carte bancaire pour le plan Free.**

---

## ÉTAPE 2 — Choisir la voix (5 minutes)

ElevenLabs a une bibliothèque de voix. Pour la darija algéroise + mix français, il faut une voix **féminine jeune multilingue avec capacité arabe**.

### Option A — Voix pré-sélectionnée recommandée (le plus simple)

Dans l'onglet **"Voices"** → **"Voice Library"** (bibliothèque), cherche dans l'ordre :

1. **"Sana"** ou **"Nadia"** ou **"Yasmine"** → voix arabes féminines jeunes (si disponibles dans la lib)
2. **"Charlotte"** → voix française jeune (bonne sur le français, correcte sur l'arabe en Multilingual v2)
3. **"Rachel"** → voix anglaise de base, étonnamment bonne en multilingue
4. **"Nicole"** → voix douce, bon rendu darija

Clique **"Add"** pour ajouter la voix à ta bibliothèque personnelle.

### Option B — Voix "Arabic" dans la Voice Library (plus authentique)

1. Dans la Voice Library, filtre par **Language = Arabic**
2. Filtre par **Gender = Female**
3. Filtre par **Age = Young**
4. Écoute 3 à 5 previews et prends celle qui sonne le plus **naturelle et jeune Alger** (pas vieille égyptienne, pas trop formelle golfe)

### Option C — Cloner une voix (le plus puissant, 10 min)

Si tu as une **créatrice algéroise sur TikTok** dont la voix te plaît :

1. Télécharge 2 à 3 minutes de ses vidéos (son clair, pas de musique de fond)
2. Dans ElevenLabs → **"Voices"** → **"Add Voice"** → **"Instant Voice Clone"**
3. Upload les fichiers audio
4. Nomme la voix "Algeroise_UGC"
5. La voix clonée est utilisable immédiatement

> **Attention légale :** cloner sans permission pour un usage commercial = risque juridique. Fais-le seulement sur ta propre voix, celle d'une proche qui a autorisé, ou une voix libre de droits.

---

## ÉTAPE 3 — Choisir le modèle (1 minute)

Dans la page de génération, choisis le modèle :

- **"Eleven Multilingual v2"** → le meilleur rapport qualité/coût pour darija+français
- **"Eleven v3 (alpha)"** → encore meilleur si disponible sur ton compte, gère les émotions
- **"Eleven Turbo v2.5"** → plus rapide mais moins bon pour l'arabe. À éviter.

**Choix recommandé : Multilingual v2.**

---

## ÉTAPE 4 — Réglages (sliders)

Dans la page de génération, règle les paramètres :

| Paramètre | Valeur recommandée | Pourquoi |
|---|---|---|
| **Stability** | 40 à 50 | Assez bas pour avoir de l'émotion naturelle, assez haut pour éviter les dérapages |
| **Similarity** | 75 à 85 | Reste fidèle à la voix choisie |
| **Style Exaggeration** | 30 à 50 | Un peu d'expressivité pour UGC, pas trop |
| **Speaker Boost** | ON | Améliore la clarté |

**Clique "Use Speaker Boost"** si l'option est disponible.

---

## ÉTAPE 5 — Textes optimisés pour ElevenLabs

**Astuce critique :** ElevenLabs lit mieux l'arabe en **écriture arabe directement** qu'en darija translittérée en lettres latines. Les mots français restent en français. Les pauses sont marquées avec `...` ou `<break time="0.5s" />` (balise SSML si supportée).

---

### VERSION 1 — Script complet (42 secondes)

Copie-colle ce texte exactement dans l'input ElevenLabs :

```
خويا... شوفي الراية تاعي. ... هادي راهي تتوسع كل شهر، والله كنت حابة نبكي.

شعري ولّى يخسر بزوج. L'oreiller صباح على صباح مليان بالشعر، ... la queue de cheval تاعي راهي داقت كي حبل. عييت من la 3attara، عييت من les masques لي يخسرو journée كاملة، و franchement قاع ما خدم والو.

كنت déjà محقّرة ندير selfie de dos، خويا. ... كنت نبغي غير la densité، شي حاجة normal، ماشي extensions، ماشي lissage، غير شعر ديالي يكبّر.

هادي اللحظة لي صاورتني. ... هاد le produit من Corée، LILYEVE Grow Turn. ... راهي ampoule بـ les exosomes تاع les plantes، ... خدمة تاع la science على les cheveux لي يتابطو. و الحاجة لي عجبتني كتر... هادي.

شوفي، la brosse راهي تتبع la raie direct، ... massage تاع la racine، ... و le sérum يوصل وين لازم. ... ما عادش نقطر في يدي، ما عادش شعري يولي دهن. ... دقيقتين غير، 3 مرات في الأسبوع.

على شهرين، ... la chute هبطات بزاف، la raie راهي ضاقت، و شوفي la queue de cheval تاعي دروك... والله ما كنتش نصدق.

خويا، matقوليش غادي، ... le LILYEVE كاين في le lien في la bio. Paiement à la livraison، livraison في 58 ولاية، ... و إذا ما عجبكش في 30 يوم راح يرجعولك فلوسك. Stock محدود، les filles راهم يتهجمو عليه.

خويتي، ... شعرك يستحق chance واحدة. ... يا الله.
```

**Nombre de caractères :** environ 1 150 (bien dans le quota gratuit).

---

### VERSION 2 — Hook court (15 secondes)

```
خويا، شوفي la raie تاعي. ... راهي تتوسع كل شهر.

جربت كل شي، والو خدم. ... حتى صاورتني هاد le Lilyeve، ... sérum تاع Corée بـ les exosomes و BROSSE direct على la racine.

شهرين غير، ... شوفي la différence. والله ما كنتش نصدق.

Lien في la bio، ... paiement à la livraison. يا الله خويا.
```

**Caractères :** ~ 350.

---

### VERSION 3 — ASMR brush focus (20 secondes)

```
كل مرة ندير هادي... ... نحس روحي مرتاحة.

La brosse تاع Lilyeve Grow Turn، ... راهي تدخل direct وين لازم، ... في la racine، على le cuir chevelu.

3 exosomes تاع les plantes، ... خدمة تاع la science على les cheveux لي يتابطو. ... Zéro gras، zéro rinçage، دقيقتين غير.

شهرين و شعرك يتبدل. ... Lien في la bio، خويا.
```

**Caractères :** ~ 450.

---

## ÉTAPE 6 — Générer et télécharger

1. Colle le texte dans le gros champ "Text"
2. Vérifie la voix sélectionnée en haut
3. Vérifie le modèle = **Multilingual v2**
4. Vérifie les sliders selon le tableau ÉTAPE 4
5. Clique **"Generate"**
6. Attends 10 à 30 secondes
7. **Écoute** le résultat
8. Si pas bon → clique **"Regenerate"** (tu peux le faire plusieurs fois, chaque régénération consomme des caractères)
9. Si bon → clique l'icône **"Download"** → télécharge en **MP3 ou WAV**

---

## ÉTAPE 7 — Corrections si le rendu n'est pas bon

**Problème : accent trop oriental (égyptien/golfe)**
→ Change de voix, prends une voix européenne multilingue (Charlotte, Rachel) qui, paradoxalement, sonnera plus "modern Alger" quand elle lira l'arabe.

**Problème : voix trop vieille**
→ Dans la Voice Library, re-filtre par **Age = Young** et teste une autre voix.

**Problème : la voix écrase le français ou l'arabe**
→ Augmente **Stability** à 60-70 et re-génère. Si c'est l'inverse (trop plat), baisse à 30-40.

**Problème : certains mots sont mal prononcés**
→ Écris-les phonétiquement en latin dans le texte. Exemple : au lieu de "Lilyeve", écris "Lili yeave" ou "Lili iv".

**Problème : les pauses sont trop longues/courtes**
→ Enlève ou ajoute des `...`. Chaque `...` ≈ 0.3 à 0.5 seconde.

---

## ÉTAPE 8 — Après génération : finitions

Télécharge ton fichier audio (généralement `elevenlabs-audio.mp3`), puis range-le dans ton workspace :

```
livrables/ecommerce/scripts-ugc/audio/
    ├── voix-off-v1-42s.mp3
    ├── voix-off-v2-15s.mp3
    └── voix-off-v3-asmr-20s.mp3
```

**Pour le montage vidéo :**
- Importe le MP3 dans CapCut, InShot, Premiere ou DaVinci
- Pose ton audio sur la timeline
- Synchronise les plans visuels aux pauses
- Ajoute une musique de fond en volume -18 à -22 dB (sous la voix off)
- Exporte en 1080x1920 (9:16) 30fps

---

## ÉTAPE 9 — Si tu veux la voix idéale sans ElevenLabs

ElevenLabs reste une maquette. Pour le lancement produit en Meta Ads sérieux, teste la vraie voix humaine en parallèle. Deux marketplaces :

- **Fiverr** → cherche "Algerian female voiceover" ou "Darija female voiceover". De 5 à 50 USD.
- **Comeup (ex-5euros.com)** → cherche "voix off algérienne". De 5 à 30 EUR.
- **Instagram DM** → cherche hashtags `#ugcalgerie`, `#creatriceugc`, `#dzcreator`. Beaucoup acceptent 2 000 à 10 000 DA par vidéo.

Si tu veux, je te prépare le brief exact à envoyer aux créatrices (prix, délais, droits de diffusion, exemples de ton attendu).

---

## Récap' en une ligne

**ElevenLabs → Sign up free → Choisir Charlotte ou voix arabe young → Modèle Multilingual v2 → Stability 45, Similarity 80 → Coller le texte version 1 (en arabe + français mélangés) → Generate → Download MP3.**

**Temps total estimé : 15 minutes.**
**Coût : 0 DA.**

---

*Fin du pack. Lance-toi, et dis-moi si un rendu te plaît ou si tu veux que j'ajuste les textes pour une voix spécifique.*
