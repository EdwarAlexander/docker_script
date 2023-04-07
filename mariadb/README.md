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

* Con salto de linea 

docker container run \
-e MARIADB_USER=example-user \
-e MARIADB_PASSWORD=user-password \
-e MARIADB_ROOT_PASSWORD=root-password \
-e MARIADB_DATABASE=world-db \
--name world-db \
-dp 3306:3306 mariadb

* Linea abreviada

docker run -e MARIADB_ROOT_PASSWORD=root-password -e MARIADB_DATABASE=world-db --name world-db -dp 3306:3306 mariadb

## Creación de contenedor con volumenes

* Creación de volumenes

docker volume create name-volumen

* Visualizar volumenes

docker volume ls

* Visualizar configuración del volumen

docker volume inspect name-volumen

* Linea abreviada

docker run -e MARIADB_ROOT_PASSWORD=root-password -e MARIADB_DATABASE=world-db --name world-db --volume name-volumen:/var/lib/mysql -dp 3306:3306 mariadb