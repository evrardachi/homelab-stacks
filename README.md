# 🧰 Infra Lab – DevOps Toolkit

Ce dépôt contient une collection de projets DevOps et homelab.

## 📦 Contenu

### 🐳 Docker
- [`zabbix-grafana`](./docker/zabbix-grafana/)
- [`wordpress`](./docker/wordpress/)

### 🌍 Terraform
- [`aws-vpc`](./terraform/aws-vpc/)
- [`ec2-instance`](./terraform/ec2-instance/)

### ☁️ AWS CLI Scripts
- [`create-bucket.sh`](./aws-cli/scripts/create-bucket.sh)
- [`deploy-app.sh`](./aws-cli/scripts/deploy-app.sh)

### 🔧 Ansible
- [`install-nginx.yml`](./ansible/playbook-install-nginx.yml)

### ⚙️ Scripts divers
- [`backup.sh`](./scripts/backup.sh)
- [`setup.py`](./scripts/setup.py)

## 🔽 Cloner et lancer un projet

```bash
git clone https://github.com/<ton-user>/infra-lab.git
cd docker/zabbix-grafana
docker compose up -d
