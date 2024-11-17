# Odoo:15 + postgress:15 Docker Compose

## Deployment
```bash
git clone https://github.com/alejandro14972/DockerCompose-odoo.git
cd odoo-docker-compose
docker-compose up -d


docker network create odoo-network
docker run --network odoo-network --name db -e POSTGRES_USER=odoo -e POSTGRES_PASSWORD=odoo -d postgres
docker run --network odoo-network -v odoo-data:/var/lib/odoo -d -p 8069:8069 --name odoo odoo
docker run --network odoo-network -v odoo-data2:/var/lib/odoo -d -p 8070:8069 --name odoo2 odoo:15


docker run -d --network odoo-network -v odoo-db:/var/lib/postgresql/data \
-e POSTGRES_USER=odoo -e POSTGRES_PASSWORD=odoo -e POSTGRES_DB=postgres \
--name db postgres:15


docker run -v odoo-data:/var/lib/odoo -d -p 8069:8069 \
--network odoo-network --name odoo odoo

docker run -v odoo-data2:/var/lib/odoo -d -p 8070:8069 \
--network odoo-network --name odoo2 odoo:15




```
