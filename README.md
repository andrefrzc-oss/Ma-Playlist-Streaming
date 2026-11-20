# Ma Playlist Streaming

Dépôt personnel de plugins natifs pour Nuvio TV. Version cible observée : **1.2.0-beta.2**.

## Ajouter le dépôt dans Nuvio TV

Dans **Paramètres → Contenu et découverte → Plugins → Ajouter un dépôt**, utiliser l'URL brute du manifeste :

`https://raw.githubusercontent.com/andrefrzc-oss/Ma-Playlist-Streaming/main/manifest.json`

## Structure

- `manifest.json` : manifeste natif Nuvio TV.
- `scrapers/authorized-source-template.js` : modèle inactif de scraper.
- `config/sites.json` : inventaire des neuf sites communiqués.

## Format des scrapers

Le runtime Nuvio TV attend un module JavaScript exportant `getStreams(tmdbId, mediaType, season, episode)` et renvoyant une liste de flux. Le modèle renvoie volontairement une liste vide.

## État des sites

Les neuf sites de `config/sites.json` sont un inventaire uniquement. Aucun connecteur n'est fourni. Avant toute intégration, vérifier les droits de diffusion, les conditions d'utilisation et l'existence d'une API ou d'un flux officiel. Ne pas contourner DRM, authentification, CAPTCHA ou restrictions d'accès.
