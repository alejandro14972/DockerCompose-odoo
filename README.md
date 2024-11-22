# Odoo:15 + postgress:15 + pgAdmin y portainer Docker Compose

## Deployment
```bash
git clone https://github.com/alejandro14972/DockerCompose-odoo.git
cd DockerCompose-odoo
mkdir proyecto
chmod -R 777 ./proyecto
chmod -R 777 ./proyecto/odoo-web-data ./proyecto/config ./proyecto/addons ./proyecto/odoo-db-data ./proyecto/portainer_data
docker-compose up -d
```
