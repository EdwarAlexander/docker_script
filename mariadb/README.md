
docker container run -e MARIADB_USER=example-user -e MARIADB_PASSWORD=user-password -e MARIADB_ROOT_PASSWORD=root-password -e MARIADB_DATABASE=world-db --name world-db -dp 3306:3306 mariadb