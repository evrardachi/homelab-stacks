# J'apprends, je teste et je vous explique

# Déploiement Typebot en Self-Hosted avec Docker

Ce projet permet de déployer une plateforme complète de chatbot visuel avec **Typebot**, en mode self-hosted, prêt à l’emploi.

## Contenu

- PostgreSQL (base de données)
- Typebot Backend (éditeur + API)
- Interface Viewer pour le rendu des bots

## Utilisation

1. Copier le fichier `.env.example` en `.env` et personnaliser les variables :

   cp .env.example .env

2. Lancer les conteneurs :

   docker compose up -d

3. Accéder aux interfaces :

| Interface          | URL               | Description                      |
| ------------------ | ----------------- | -------------------------------- |
| Editeur Typebot    | http://<@IP>:8080 | Crée et édite tes bots           |
| Viewer (rendu bot) | http://<@IP>:8081 | Aperçu et test des conversations |

## Authentification GitHub

Créer une OAuth App dans GitHub :

- Homepage URL : `http://<@IP>:8080`
- Callback URL : `http://<@IP>:8080/api/auth/callback/github`

Configurer ensuite dans `.env` :

GITHUB_CLIENT_ID=...
GITHUB_CLIENT_SECRET=...
NEXTAUTH_URL=http://<@IP>:8080

## Nettoyage

docker compose down -v

## Structure

- `docker-compose.yml` : définition des services Docker
- `.env.example` : fichier de configuration à adapter
- `README.md` : documentation d’installation
