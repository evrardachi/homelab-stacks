# J'apprends, je teste et je vous explique

# Déploiement Zabbix + Grafana avec Docker Compose

Ce projet permet de déployer une stack complète de supervision avec **Zabbix** + **Grafana**, interconnectés automatiquement.

## Contenu

- PostgreSQL (base de données Zabbix)
- Zabbix Server
- Zabbix Web Interface
- Grafana avec plugin Zabbix

## Utilisation

1. Copier le fichier `.env.example` en `.env` :

   cp .env.example .env

2. Lancer la stack :

   docker compose up -d

3. Accéder aux interfaces :

| Interface  | URL                              | Identifiants   |
| ---------- | -------------------------------- | -------------- |
| Zabbix Web | http://<@adresse_ip_server>:8080 | Admin / zabbix |
| Grafana    | http://<@adresse_ip_server>:3000 | admin / admin  |

## Nettoyage

docker compose down -v

## Structure

- `docker-compose.yml` : définition des services
- `.env.example` : configuration à adapter
- `README.md` : documentation
