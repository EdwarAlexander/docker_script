# Comando para imagen de docker

* crear contenedor de servidor de base de datos postgres
 
docker run --name db-postgres -e POSTGRES_PASSWORD=123456 -d -p 5432:5432 postgres