# Creación de contenedor de BD Mariadb
## Descargar la imagen oficial de Mariabd

docker pull mariadb

## Creación de contenedor en una sola linea

* En una sola linea

docker container run --env MARIADB_ROOT_PASSWORD=root-password --env MARIADB_DATABASE=world-db --name world-db -dp 3306:3306 mariadb

* Con variable de entorno abreviado

docker container run -e MARIADB_ROOT_PASSWORD=root-password -e MARIADB_DATABASE=world-db --name world-db -dp 3306:3306 mariadb

* Con variable de entorno de creación de usuario 

docker container run -e MARIADB_USER=example-user -e MARIADB_PASSWORD=user-password -e MARIADB_ROOT_PASSWORD=root-password -e MARIADB_DATABASE=world-db --name world-db -dp 3306:3306 mariadb