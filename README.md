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
## Create odoo 
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

## Settings to connect Oddo to PgAdmin
```bash
Add new server
--General
  name: conexion
--Connection
  Host: db
  Port:5432
  Maintenance database: postgres
  username: odoo
  password: odoo
```


## Install from GitHub Plan general Contable Español
```bash
  https://github.com/OCA/l10n-spain/tree/15.0   (I recommend download zip)
  pip install -r requirements.txt
  copy it to folder 'addons'
  activate developer mode
  update applications
  search 'España - Contabilidad (PCGE 2008)'
  same for toponyms (https://github.com/OCA/partner-contact/tree/15.0)
  copy only to addons folder called base_location_geonames_import
```
