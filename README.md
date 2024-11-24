# Odoo:15 + postgress:15 + pgAdmin y portainer Docker Compose

## Deployment
```bash
git clone https://github.com/alejandro14972/DockerCompose-odoo.git
cd DockerCompose-odoo
mkdir proyecto
chmod -R 777 ./proyecto
docker-compose up -d
chmod -R 777 ./proyecto/odoo-web-data ./proyecto/config ./proyecto/addons ./proyecto/odoo-db-data ./proyecto/portainer_data
```
## Settings
```bash
cd proyecto
cd congig
nano odoo.conf
addons_path = DockerCompose-odoo/proyecto/addons,/mnt/extra-addons
```
