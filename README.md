# n8n WhatsApp Prospection

> Workflows n8n open source pour automatiser une partie de la prospection des PME sur WhatsApp et Meta, en gardant un humain dans la boucle.
> *Open-source n8n workflows for semi-automated WhatsApp & Meta prospecting, built for SMEs in francophone Africa.*

🇫🇷 Français · [🇬🇧 English](#english)

---

## Pourquoi ce projet

En Afrique francophone, la majorité des ventes des PME passent par WhatsApp. Les prospects arrivent depuis Facebook, Instagram ou une publicité Meta, puis la conversation se fait à la main, souvent sans suivi. Résultat : des leads perdus, des relances oubliées et aucun historique.

Ce projet fournit des **workflows n8n prêts à importer** pour :

- récupérer automatiquement les leads (publicités Meta, formulaires, messages entrants) ;
- les centraliser dans un tableau de suivi ;
- qualifier les demandes avec une IA ;
- préparer des réponses et des relances qu'**un humain valide avant l'envoi**.

**Semi-automatisé, pas un robot de spam.** Chaque premier message sortant passe par une validation humaine, et le projet utilise uniquement l'API officielle de WhatsApp Business.

## Statut

🚧 **En développement.** Les workflows sont publiés au fur et à mesure. Voir la [feuille de route](#feuille-de-route).

## Fonctionnalités prévues

| Module | Description | Statut |
|---|---|---|
| `01-capture-leads` | Récupère les leads Meta Lead Ads et les messages WhatsApp entrants | ⏳ À venir |
| `02-crm-sheets` | Enregistre et met à jour chaque lead dans Google Sheets | ⏳ À venir |
| `03-qualification-ia` | Classe le lead (chaud / tiède / froid) et résume sa demande | ⏳ À venir |
| `04-reponse-validee` | Propose une réponse ; l'envoi se fait après validation humaine | ⏳ À venir |
| `05-relances` | Programme des relances avec des modèles approuvés par Meta | ⏳ À venir |
| `06-rapport` | Envoie un récapitulatif quotidien des leads et conversions | ⏳ À venir |

## Prérequis

- [n8n](https://n8n.io) auto-hébergé (Docker conseillé) ou n8n Cloud
- Un compte **WhatsApp Business Platform (Cloud API)** relié à un compte Meta Business vérifié
- Un compte Google pour Google Sheets
- Une clé API d'un fournisseur d'IA (Claude, OpenAI ou autre)

## Installation rapide

```bash
git clone https://github.com/lenoir07/n8n-whatsapp-prospection.git
cd n8n-whatsapp-prospection
cp .env.example .env   # puis remplis tes propres valeurs
```

1. Ouvre n8n, puis **Workflows → Importer depuis un fichier**.
2. Importe les fichiers du dossier `workflows/` dans l'ordre (01, 02, …).
3. Configure tes identifiants dans n8n (**Credentials**) ; ne les mets jamais dans les fichiers JSON.
4. Suis le guide détaillé : [`docs/installation.md`](docs/installation.md).

## Structure du dépôt

```
n8n-whatsapp-prospection/
├── workflows/          # Workflows n8n exportés (.json), numérotés par étape
├── templates/
│   └── messages/       # Modèles de messages WhatsApp (FR / EN)
├── docs/               # Guides : installation, configuration Meta, conformité
├── scripts/            # Petits utilitaires (export, vérification)
├── .env.example        # Variables d'environnement à copier
├── CONTRIBUTING.md     # Comment contribuer
└── LICENSE             # Licence MIT
```

## Bonnes pratiques et conformité

- **Consentement obligatoire** : n'écris qu'aux personnes qui t'ont contacté ou qui ont accepté d'être recontactées.
- **Fenêtre de 24 heures** : en dehors de cette fenêtre, WhatsApp n'autorise que des modèles de messages approuvés par Meta.
- **Pas de bibliothèques non officielles** : elles exposent le numéro à un bannissement.
- **Données personnelles** : respecte la loi en vigueur dans ton pays (au Bénin, le Code du numérique) et ne publie jamais de vraies données de clients dans ce dépôt.

## Feuille de route

- [ ] Module 01 : capture des leads
- [ ] Module 02 : CRM Google Sheets
- [ ] Module 03 : qualification IA
- [ ] Module 04 : réponse validée par un humain
- [ ] Module 05 : relances
- [ ] Module 06 : rapport quotidien
- [ ] Tutoriels vidéo en français
- [ ] Traduction complète en anglais

## Contribuer

Les contributions sont les bienvenues : nouveaux workflows, corrections, traductions et documentation. Lis [`CONTRIBUTING.md`](CONTRIBUTING.md) avant d'ouvrir une pull request.

## Auteur

**Victor GBEDONOU** ([@lenoir07](https://github.com/lenoir07)), Cotonou, Bénin
Marketing digital, motion design et automatisation pour les PME.

## Licence

[MIT](LICENSE) : libre d'utilisation, de modification et de redistribution.

---

## English

**n8n WhatsApp Prospection** is a set of open-source n8n workflows that help small businesses in francophone Africa capture leads from Meta ads and WhatsApp, track them in Google Sheets, qualify them with AI, and draft replies and follow-ups that **a human approves before sending**.

It uses only the official WhatsApp Business Cloud API, requires recipient consent, and is not a bulk-messaging tool.

**Status:** work in progress, see the roadmap above. Contributions (workflows, docs, translations) are welcome; see [`CONTRIBUTING.md`](CONTRIBUTING.md).
