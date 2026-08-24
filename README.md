# Praeparo — version publiée

**Essayer : <https://prettozm.github.io/Praeparo-public/>**

Praeparo est un atelier visuel pour concevoir, matérialiser et vérifier les workflows de travail entre humains, agents IA et outils.

Ce dépôt ne contient que la **version publiée** : une page HTML unique, autonome (aucun backend, aucun service externe — vos projets restent dans votre navigateur), et le **package de distribution** officiel. Le code source vit dans un dépôt privé ; ces artefacts y sont produits par :

```bash
npm run build && node scripts/build-single-file.mjs
# → apps/studio/dist/praeparo-standalone.html, copié ici en index.html
npm run package:bootstrap
# → distribution/manifest.json + praeparo-bootstrap-<version>.zip, copiés ici
```

## Configurer votre projet avec Praeparo

Le parcours principal passe par votre agent de développement (Claude Code, ou tout agent capable de lire un dépôt) : sur la page publiée, « **Configurer mon projet avec Praeparo** » fournit un prompt à copier dans l'agent. Il récupère le package officiel, vérifie son intégrité, installe ou met à niveau `.praeparo/` sans toucher à vos données, puis mène la configuration en conversation.

## Distribution

- Manifest (source de vérité) : [`distribution/manifest.json`](distribution/manifest.json) — version publiée, package exact, empreinte SHA-256.
- Package versionné : `distribution/praeparo-bootstrap-<version>.zip` (uniquement des chemins sous `.praeparo/` ; son protocole d'installation est dans l'archive).
- `distribution/praeparo-bootstrap-latest.zip` est une commodité, jamais la source de vérité.

## Notes d'utilisation

- Vos projets sont enregistrés localement dans votre navigateur ; utilisez « Exporter praeparo.yml » (téléchargement ou copier-coller) pour les versionner.
- La connexion d'un dossier local (Inspect/Compile sur un vrai dépôt) nécessite Chrome ou Edge.
