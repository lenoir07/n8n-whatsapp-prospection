# Installation

> Guide en cours de rédaction. Il sera complété au fil de la publication des workflows.

## 1. Installer n8n avec Docker

```bash
docker run -it --rm --name n8n -p 5678:5678 \
  -v n8n_data:/home/node/.n8n \
  docker.n8n.io/n8nio/n8n
```

Ouvre ensuite http://localhost:5678.

Pour recevoir les webhooks de WhatsApp, n8n doit être joignable en HTTPS depuis Internet (serveur VPS ou n8n Cloud).

## 2. Configurer WhatsApp Business Cloud API

- [ ] Créer une app sur Meta for Developers
- [ ] Ajouter le produit WhatsApp et relier un numéro
- [ ] Générer un jeton d'accès permanent (utilisateur système)
- [ ] Déclarer l'URL du webhook n8n et le jeton de vérification

## 3. Préparer Google Sheets

- [ ] Dupliquer le modèle de tableau (lien à venir)
- [ ] Connecter Google Sheets dans les Credentials de n8n

## 4. Importer les workflows

Importe les fichiers du dossier `workflows/` dans l'ordre, puis associe tes Credentials à chaque nœud.
