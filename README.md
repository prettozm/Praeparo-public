# Praeparo — version publiée

**Essayer : <https://prettozm.github.io/Praeparo-public/>**

Praeparo est un atelier visuel pour concevoir, matérialiser et vérifier les workflows de travail entre humains, agents IA et outils.

Ce dépôt ne contient que la **version publiée** : une page HTML unique, autonome (aucun backend, aucun service externe — vos projets restent dans votre navigateur). Le code source vit dans un dépôt privé ; cette page y est produite par :

```bash
npm run build && node scripts/build-single-file.mjs
# → apps/studio/dist/praeparo-standalone.html, copié ici en index.html
```

## Notes d'utilisation

- Vos projets sont enregistrés localement dans votre navigateur ; utilisez « Exporter praeparo.yml » (téléchargement ou copier-coller) pour les versionner.
- La connexion d'un dossier local (Inspect/Compile sur un vrai dépôt) nécessite Chrome ou Edge.
