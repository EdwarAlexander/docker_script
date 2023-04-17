# Comandos basicos de docker

* Visualizar los logs de los contenedores

docker container logs -f id-contenedor

* Ingresar a la consola del contenedor

docker exec -it id-contenedor /bin/sh

* Borrar todas las imagenes de forma forzada

docker image prune -a 