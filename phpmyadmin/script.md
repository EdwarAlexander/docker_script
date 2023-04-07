# Creación de contenedor de phpmyadmin 5.2.0
## Descargar la imagen oficial

docker pull phpmyadmin:5.2.0-apache

## Creación de contenedor

docker run --name phpmyadmin -d -e PMA_ARBITRARY=1 -p 8080:80 phpmyadmin:5.2.0-apache