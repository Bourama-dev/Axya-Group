# Axya Group — axyagroup.fr

Landing page vitrine de la holding Axya Group, renvoyant vers ses deux projets :
[CléAvenir](https://cleavenir.com) et [Hakily](https://hakily.fr).

## Stack

HTML/CSS vanilla, une seule page. Pas de framework (Next.js, etc.) : le site est
une seule page statique sans état, sans routing dynamique et sans besoin de
build — un framework n'apporterait ici que de la complexité de déploiement pour
aucun bénéfice.

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
