# JUDE — Site officiel (jude-music.com)

Site statique, prêt à déposer sur GitHub Pages. Deux écrans (comme jorjasmith.com).

## Structure
- `index.html` — écran d'entrée plein écran (EVERGREEN). Boutons : Voir le clip / Écouter / Entrer sur le site.
- `home.html` — site complet : bio, discographie, clips, écouter, live/tour, boutique, newsletter, contact.
- `assets/` — logo, goutte (favicon), image cinématique, photo, image de partage.

## Ce qui est déjà intégré
- **Logo** JUDE (script rouge) dans la nav, le hero, le footer, la popup ; **goutte** en favicon.
- **Image de fond** de l'écran d'entrée : la bannière cinématique (`assets/banner.jpg`).
- **Photo hero** du site : la photo de Philomène (`assets/jude-photo.jpg`).
- **Image de partage** (réseaux) : `assets/og-cover.jpg` (photo + logo).
- **Vidéos** : teaser Evergreen (youtu.be/oQS_yDBMZAU) et Live Session (youtu.be/WtZPowp8_MM),
  avec leurs miniatures YouTube.
- **Vidéo de fond** de l'écran d'entrée : `assets/evergreen-loop.mp4` (en boucle, muette).
- **Newsletter** : branchée sur ton formulaire **Kit** (form 9560377). Voir ci-dessous.

## Newsletter Kit — à tester une fois en ligne
La popup envoie directement vers ton formulaire Kit `9560377` (script officiel `ck.5.js`).
Les inscrits tombent dans ta liste Kit et reçoivent ton email de confirmation (double opt-in).
➡️ Après mise en ligne, fais **un test réel** : ouvre la popup, inscris une adresse, et vérifie
qu'elle apparaît dans Kit + que l'email de confirmation arrive. Si jamais l'affichage du message
de succès ne te convient pas, on pourra ajuster.
(Le champ « Pays » n'a pas été inclus car il n'existe pas par défaut dans Kit ; on peut l'ajouter
en créant un *custom field* `country` côté Kit.)

## Bilingue FR / EN
Le site est entièrement bilingue : bouton FR / EN en haut à droite (sur les 2 pages).

## Liens branchés ✅
- Écouter / smart-link : https://ffm.bio/jude-music
- Discographie : Evergreen, Bain Rouge, I AM! → leurs clips YouTube
- Vidéos : teaser Evergreen, Live Session Paper Street, Live Session Solo
- Boutique : https://judeofficialmusic.bandcamp.com/
- Concerts : widget Bandsintown (artiste 15607522) — à vérifier une fois en ligne

## Ce qu'il reste à brancher (liens)
Cherche les `href="#"` :
- **Écouter** (écran d'entrée + section Écouter) : smart-link et profils Spotify / Apple / Deezer.
- **Boutique** : lien Bandcamp / Shopify.
- **Dates de concert** : section `#tour` de `home.html` (un exemple est en commentaire).
- Le bouton « Voir le clip » pointe sur le **teaser** ; remplace-le par le clip complet à sa sortie.

## Vidéo de fond animée — intégrée ✅
L'écran d'entrée joue `assets/evergreen-loop.mp4` (720p optimisée, ~3,6 Mo, muette, en boucle),
avec `assets/evergreen-poster.jpg` en image de secours pendant le chargement. La lecture auto
respecte le réglage « réduire les animations » (la vidéo se fige alors sur le poster).

## Déploiement GitHub Pages
1. Repo **public** → dépose le **contenu** de ce dossier à la racine.
2. Settings → Pages → branche `main`, dossier `/ (root)`.
3. Custom domain : `jude-music.com` + **Enforce HTTPS**.
4. DNS : A records `185.199.108.153 / .109 / .110 / .111`, et CNAME `www → TON-PSEUDO.github.io`.

## Après mise en ligne
- Google Search Console : soumets `sitemap.xml`.
- Vérifie l'aperçu de partage sur opengraph.xyz.
