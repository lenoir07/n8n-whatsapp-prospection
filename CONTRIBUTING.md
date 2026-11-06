# Contribuer · Contributing

Merci de ton intérêt ! *Thanks for your interest! English contributions are welcome.*

## Comment contribuer

1. **Forke** le dépôt, puis crée une branche : `git checkout -b feat/nom-de-ta-modif`.
2. Fais tes modifications.
3. Ouvre une **pull request** qui explique ce que tu as changé et pourquoi.

## Règles pour les workflows

- Exporte le workflow depuis n8n (**Télécharger**) et place le `.json` dans `workflows/`.
- Nomme le fichier ainsi : `NN-nom-court.json` (ex. `03-qualification-ia.json`).
- **Supprime toutes les données sensibles avant l'export** : jetons, numéros de téléphone, ID de compte, données clients.
- Utilise les **Credentials** de n8n, jamais de clés écrites en dur.
- Ajoute une note (*Sticky Note*) dans le workflow pour expliquer chaque étape.
- Documente le workflow dans `docs/`.

## Ce qui est refusé

- Les fonctions d'envoi massif ou de prospection sans consentement.
- Les intégrations à des bibliothèques WhatsApp non officielles.
- Les fichiers contenant de vraies données personnelles.

## Signaler un problème

Ouvre une **issue** en indiquant ta version de n8n, le workflow concerné, ce que tu attendais et ce qui s'est passé (avec une capture si possible, sans données sensibles).
