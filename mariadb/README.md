# Creación de contenedor de BD Mariadb
## Descargar la imagen oficial de Mariabd

docker pull mariadb

## Creación de contenedor en una sola linea

docker container run -e MARIADB_USER=example-user -e MARIADB_PASSWORD=user-password -e MARIADB_ROOT_PASSWORD=root-password -e MARIADB_DATABASE=world-db --name world-db -dp 3306:3306 mariadb