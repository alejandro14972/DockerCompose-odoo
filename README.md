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
## To create odoo 
```bash
http://localhost:8069/
````
## Settings to install modules in odoo
```bash
cd proyecto
cd congig
nano odoo.conf
addons_path = /usr/lib/python3/dist-packages/odoo/addons, /mnt/extra-addons
```
