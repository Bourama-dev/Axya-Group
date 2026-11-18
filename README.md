# Axya Group — axyagroup.fr

Landing page vitrine de la holding Axya Group, renvoyant vers ses deux projets :
[CléAvenir](https://cleavenir.com) et [Hakily](https://hakily.fr).

## Stack

HTML/CSS vanilla, une seule page. Pas de framework (Next.js, etc.) : le site est
une seule page statique sans état, sans routing dynamique et sans besoin de
build — un framework n'apporterait ici que de la complexité de déploiement pour
aucun bénéfice.

## Design

Charte Axya : fond bleu nuit, dégradés bleu → cyan → violet, wordmark AXYA
(X en dégradé) avec la ligne « GROUP ». La page d'accueil suit la maquette du
hero : navigation avec indicateur actif qui glisse, scène des trois mascottes
(Axi pour Axya, la chouette pour Hakily, le panda roux pour CléAvenir), cartes
flottantes, compteurs et vague de particules animée (canvas).

Motion design : entrées échelonnées, parallaxe des mascottes à la souris,
arc lumineux en rotation, cartes inclinées en 3D, boutons magnétiques,
manifeste révélé mot à mot, étapes avec rail de progression, bandeaux
défilants. Tout est désactivé si l'utilisateur a demandé moins d'animations
(`prefers-reduced-motion`).

Vidéo : `assets/axya-group.mp4` (poster `assets/axya-group-poster.jpg`) est
intégrée dans la section « En vidéo » sous les marques, et le bouton « Voir la
vidéo » du hero l'ouvre dans une modale (attribut `data-src` du
`<dialog id="video">`).

Images des mascottes : `assets/axi-700.webp`, `assets/hakily-owl.webp`,
`assets/cleavenir-panda.webp`, `assets/mascots-trio.webp` (`assets/axi.webp`
est la version haute définition d'Axi).

## Structure

```
index.html                 page d'accueil
mentions-legales/index.html  page mentions légales (URL propre : /mentions-legales/)
assets/                     images (logos, favicon, og-image)
robots.txt
sitemap.xml
```

## Déploiement

Site 100% statique : déployable tel quel sur Vercel, Netlify, GitHub Pages, ou
tout hébergeur mutualisé (OVH, etc.) en copiant les fichiers à la racine du
document root. Aucune étape de build nécessaire.

## Assets manquants

Le dossier `assets/` doit contenir :
- `cleavenir-logo.png`, `hakily-logo.png` (fournis par le porteur de projet)
- `favicon.ico`, `favicon.svg`, `apple-touch-icon.png`, `site.webmanifest`
  (à générer à partir du logo Axya Group une fois fourni)
- `og-image.png` (1200×630, pour le partage sur les réseaux sociaux)

## Mentions légales

Les informations d'identité de l'éditeur, l'hébergeur et le SIREN sont à
compléter dans `mentions-legales/index.html` (marqués `[À COMPLÉTER]`) avant
la mise en production.
