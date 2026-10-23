# Prompt Claude Design — Site produit Liva (template e-commerce landing)

> Prompt complet basé sur l'architecture du PDF : Hero → Magazines → Bénéfices → Avant/Après → Avis bénéfice → Section produit → Utilisation → Avis clients → FAQ → Contact → Footer.
> Prêt à coller dans Claude Design (ou Lovable, v0, Framer AI).
> Les placeholders `[À REMPLIR]` sont à compléter avant génération.

---

## Avant de coller

**Remplis d'abord ces 7 infos dans le prompt ci-dessous (fais Ctrl+F sur `[À REMPLIR` pour les trouver vite) :**

1. **Produit Liva** : nom exact, catégorie
2. **Prix** : normal + promo
3. **Proposition de valeur unique** (titre Hero) : 1 phrase punchy
4. **Les 6 bénéfices** : liste courte
5. **Médias dispo** : photo produit, avant/après, avis clients, logo
6. **Logos magazine** : vrais ou laisser des exemples
7. **SAV** : email + horaires

Si tu n'as pas une info, laisse le placeholder, Claude Design mettra un visuel générique que tu remplaceras ensuite.

---

## PROMPT À COLLER

```
Cree-moi un site e-commerce landing page mono-produit, moderne et vendeur, pour la marque Liva. L'objectif unique : convertir le visiteur en client (achat ou prise de contact). Design mobile-first, direct, agressivement orienté conversion. Pas de blog, pas de menu complexe, pas d'autres produits : UN SEUL produit, UNE SEULE page.

J'ai attache mes photos et logo au message. Utilise-les en priorite. Si une photo manque, mets un placeholder gris propre avec un label "Photo a inserer".

===========================
1. CONTEXTE MARQUE
===========================

Nom de la marque : Liva
Produit : [A REMPLIR : nom exact du produit, categorie, ex: "Huile capillaire naturelle pour la pousse"]
Pays cible : Algerie (marche principal) + diaspora algerienne en France
Positionnement : [A REMPLIR : premium naturel ? haut de gamme ? accessible pop ? medical ?]
Proposition de valeur unique (promesse en 1 phrase) : [A REMPLIR : ex "L'huile qui fait repousser tes cheveux visiblement en 30 jours"]

Prix affiche : 
- Prix normal : [A REMPLIR] DA
- Prix promo : [A REMPLIR] DA (barre le normal, mets le promo en gros)
- Raison de la promo : [A REMPLIR : "lancement", "stock limite", "offre speciale weekend"...]
- Urgence : [A REMPLIR : "Plus que X unites en stock", "Promo valable 48h", etc]
- Bundle : [A REMPLIR : "Pack 3 flacons -20%" ou similaire si applicable]

===========================
2. STRUCTURE DU SITE (11 sections dans l'ordre)
===========================

SECTION 1 — HEADER + HERO BANNIERE
- Header fin, sticky au scroll : menu burger a gauche (3 traits), LOGO Liva centre, panier a droite (icone)
- Hero plein ecran (100vh) :
  - A gauche : image produit (packshot photo du produit sur fond neutre)
  - A droite : grand titre = la proposition de valeur unique
  - Sous-titre : phrase complementaire courte
  - 2 CTA cote a cote : "Commander maintenant" (bouton principal plein, couleur accent) + "Decouvrir" (bouton outline, lien vers section #produit)
  - Petite reassurance sous les CTA : "Livraison 48h en Algerie · Paiement a la livraison · 1500+ clients satisfaits"
- Sur mobile : image produit en haut, texte dessous, CTAs empiles

SECTION 2 — BANDEAU "VU DANS" (logos magazine)
- Petit bandeau horizontal fin, fond blanc ou gris clair
- Mention a gauche : "VU DANS" en petites majuscules
- Logos magazine en noir et blanc (grayscale), tous a la meme hauteur, espacement regulier
- [A REMPLIR : liste des magazines a afficher, ex pour l'Algerie : Liberte, El Watan, TSA, Ennahar, Dzeriet, Vogue Arabia]
- Si placeholders, Claude Design met des logos genericques "MAGAZINE 1, MAGAZINE 2..."

SECTION 3 — MISE EN AVANT 6 BENEFICES (grille autour image produit)
- Layout : 3 benefices a gauche, image produit au centre (grande), 3 benefices a droite
- Sur mobile : image produit en haut, 6 benefices en grille 2x3 dessous
- Chaque benefice = petite card noire avec texte blanc, 1 ligne courte, taille uniforme
- [A REMPLIR : les 6 benefices courts, ex : "100% naturel", "Resultats en 15 jours", "Sans paraben", "Fabrique en Algerie", "Testé dermatologiquement", "Garantie satisfait ou rembourse"]

SECTION 4 — AVANT / APRES (preuve visuelle)
- Grand titre : "La difference en [X jours/semaines]"
- 2 photos cote a cote avec labels "AVANT" et "APRES" au-dessus
- Au milieu entre les 2 photos : icone petite fleche ou slider horizontal
- Si Claude Design peut faire un vrai slider interactif (drag pour comparer), encore mieux
- [A REMPLIR : "Photos avant/apres disponibles ? OUI/NON. Si NON, mets placeholder gris avec label 'Photo avant/apres a venir'"]

SECTION 5 — AVIS CLIENTS BENEFICE (3 cartes mise en avant)
- Titre section : "Ils ont vu la difference"
- 3 cartes cote a cote (empilees sur mobile) avec :
  - Photo profil ronde ou avatar lettre
  - 5 etoiles jaunes
  - Court temoignage (1-2 phrases)
  - Nom + ville + type de projet
- [A REMPLIR : "Avis clients disponibles ? OUI/NON. Si NON, mets 3 temoignages placeholder credibles pour le produit"]

SECTION 6 — SECTION PRODUIT (le coeur du site, bloc de conversion)
- Grand bloc centre, fond gris clair ou blanc avec border
- A gauche : grande image produit (ou carousel 3-4 images)
- A droite : bloc d'achat avec dans l'ordre :
  - Note globale : 5 etoiles + "4.9/5 (328 avis)"
  - Nom du produit en grand, bold
  - Prix : prix barre + prix promo en gros rouge
  - Raison de la promo (petit badge rouge) : "-30% Promo lancement"
  - Compteur d'urgence : "⏳ Plus que [X] unites en stock" (compteur fictif qui descend tres lentement si Claude Design peut)
  - Bundle (3 options radio) :
    * 1 flacon : [prix1] DA
    * 2 flacons : [prix2] DA (-15%) RECOMMANDE
    * 3 flacons : [prix3] DA (-25%) MEILLEURE OFFRE
  - Reassurance en bullet points :
    * Livraison 48h partout en Algerie
    * Paiement a la livraison (COD)
    * Satisfait ou rembourse 30 jours
    * SAV WhatsApp 7j/7
  - CTA visible gros bouton : "COMMANDER MAINTENANT - [prix] DA"
  - Petit lien dessous : "Ou commander par WhatsApp"

SECTION 7 — UTILISATION / INGREDIENTS (3 cartes horizontales)
- Titre section : "Comment ca marche" ou "Nos ingredients"
- 3 cartes cote a cote avec image + titre + courte description
- [A REMPLIR : "Si produit = cosmetique, parler des 3 ingredients principaux. Si produit = objet, parler des 3 etapes d'utilisation"]
- Ex pour une huile : "Huile d'argan BIO" + "Vitamine E" + "Extrait de romarin"
- Ex pour un objet : "Etape 1 : deballage" + "Etape 2 : utilisation" + "Etape 3 : rangement"

SECTION 8 — AVIS CLIENTS (style Google Reviews, scrollable)
- Titre section : "Ce qu'en disent nos clients" + petit widget "⭐ 4.9/5 - 1328 avis"
- Grille ou carousel horizontal de 6 a 9 avis clients
- Chaque avis : etoiles + photo client (ou screenshot WhatsApp si Claude Design peut imiter) + nom + verified badge + texte
- Si possible : filtres par note en haut (5 etoiles, 4 etoiles...)
- Design inspire des reviews Shopify (Loox, Judge.me, Yotpo)

SECTION 9 — FAQ (accordeon)
- Titre : "Vos questions"
- Liste de 5 a 7 questions en accordeon (details/summary HTML)
- Questions a inclure :
  * Combien de temps avant de voir les resultats ?
  * Y a-t-il des effets secondaires ?
  * Comment se passe la livraison ?
  * Puis-je etre rembourse si je ne suis pas satisfait ?
  * Est-ce que le produit convient a [cible] ?
  * Comment utiliser le produit correctement ?
  * Puis-je payer a la livraison ?

SECTION 10 — NOUS CONTACTER (formulaire court)
- Grand titre : "Une question ?"
- Sous-titre : "Ecrivez-nous via le formulaire ou directement sur WhatsApp, on repond sous 15 minutes"
- Formulaire 3 champs : Nom + Email + Message (textarea)
- Bouton principal : "Envoyer le message" (couleur accent)
- Alternative : gros bouton WhatsApp vert a cote avec icone "Discuter sur WhatsApp"

SECTION 11 — FOOTER (pied de page)
- Fond noir, texte blanc
- 3 colonnes :
  * Colonne 1 : Logo Liva + courte phrase + reseaux sociaux (Instagram, TikTok, Facebook)
  * Colonne 2 : Liens legaux (CGV, Mentions legales, Politique de confidentialite, Politique de retour)
  * Colonne 3 : Contact (email SAV, telephone, horaires)
- Barre tout en bas : "© 2026 Liva. Tous droits reserves."

===========================
3. BOUTON WHATSAPP FLOTTANT
===========================

Bouton rond vert WhatsApp fixe en bas a droite, visible sur toutes les sections pendant le scroll. Pulse legerement. Clic ouvre WhatsApp avec message pre-rempli : "Bonjour Liva, je suis interesse(e) par votre produit."

===========================
4. DESIGN ET IDENTITE
===========================

Palette couleurs : [A REMPLIR : si Liva a deja une charte, decris-la. Sinon je propose :]
- Dominante : noir profond #0A0A0A + blanc #FFFFFF
- Accent principal : [A REMPLIR : rouge chaud ? dore ? vert ? rose ?]
- Vert WhatsApp #25D366 UNIQUEMENT pour boutons WhatsApp
- Jaune doré #FFB800 pour les etoiles

Typographie :
- Titres : sans-serif moderne bold (Poppins, Inter, Space Grotesk)
- Corps : sans-serif lisible (Inter, Open Sans)
- Prix et chiffres : font bolder pour impact

Style general :
- Mobile-first obligatoire (80%+ trafic sera mobile en Algerie)
- Beaucoup d'espace blanc, respirabilite
- Micro-animations douces au scroll (fade-in, pas de parallax lourd)
- CTA toujours visibles, couleur accent qui ressort
- Pas d'elements qui bougent trop (pas de carousel auto-rotate agressif)

===========================
5. CONFIGURATION TECHNIQUE
===========================

- Prevoir integration Shopify : le CTA "Commander maintenant" doit pouvoir rediriger vers une page produit Shopify
- Pixel Meta prepare (placeholder a remplir plus tard)
- Google Analytics 4 prepare (placeholder)
- WhatsApp Business number : [A REMPLIR : numero WhatsApp Liva en format +213XXXXXXXXX]
- Email SAV : [A REMPLIR : email contact@liva.dz ou similaire]
- Horaires SAV : [A REMPLIR : ex "Samedi-Jeudi, 9h-18h"]

===========================
6. SEO
===========================

Title tag : "Liva - [A REMPLIR : produit] | [promesse courte]"
Meta description : "[A REMPLIR : 150 caracteres max avec promesse + CTA]"

Mots-cles a integrer naturellement :
- [A REMPLIR : liste des 5-10 mots-cles pertinents]

===========================
7. CE QUI NE DOIT PAS APPARAITRE
===========================

- Pas de blog ni d'articles
- Pas de menu avec sous-pages (c'est une landing page)
- Pas d'autres produits visibles (focus 100% sur le produit Liva)
- Pas de carousel auto-rotate agressif
- Pas de pop-up intrusif a l'ouverture (newsletter OK a 30s de scroll max)
- Pas de tirets longs (em dashes), uniquement tirets courts et virgules
- Pas de langue anglaise (francais principal, arabe simple si pertinent)

===========================
8. LIVRABLES ATTENDUS
===========================

Genere :
1. Site mono-page complet, responsive, mobile-first
2. HTML + CSS + JS vanilla (pas de framework lourd)
3. Les 11 sections dans l'ordre decrit
4. Prêt a hoster partout (Shopify, Netlify, GitHub Pages, hebergeur classique)
5. Code commenté, propre, exportable

Si tu as un choix stylistique a faire non specifie, prends la decision la plus premium et la plus orientee conversion possible.

GO.
```

---

## Après avoir généré le site dans Claude Design

**1. Remplace les placeholders restants :**
- Numéro WhatsApp
- Email SAV
- Prix exacts
- Vraies photos (upload direct dans Claude Design)
- Vrais avis clients

**2. Teste sur mobile en priorité** (80% du trafic Algérie)

**3. Deux options d'hébergement :**

**Option A — Shopify (recommandé pour vendre en ligne)**
Je t'accompagne pour :
- Créer le compte Shopify (si pas déjà fait)
- Choisir un thème qui ressemble au design généré, OU importer le HTML custom
- Configurer le produit (nom, prix, variantes bundle, images)
- Activer "Paiement à la livraison" (COD) pour l'Algérie
- Connecter ton domaine `.dz` ou `.com` au Shopify

**Option B — Hébergement statique (Netlify ou GitHub Pages)**
Moins cher mais pas de panier/paiement intégré. Tu renvoies vers WhatsApp pour commander.

---

## Prochaines étapes

Quand tu auras rempli les placeholders et généré le site dans Claude Design :
1. Dis-moi "le site Liva est généré"
2. Je te guide pour le mettre sur Shopify étape par étape

Et dis-moi aussi :
- As-tu déjà un **compte Shopify actif** pour Liva ?
- As-tu un **nom de domaine** pour Liva (ex: liva.dz, liva.com) ?
- As-tu un **compte WhatsApp Business** dédié Liva ou tu réutilises un existant ?
