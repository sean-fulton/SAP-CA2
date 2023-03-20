
# Main

```
// create a docker network.

docker network create mydockernetwork

// run mysql:latest docker image with the name of db and root password=my-secret-password.

docker run --network mydockernetwork -e MYSQL_ROOT_PASSWORD=my-secret-password --name mysql -d mysql:latest

// run the docker image phpmyadmin/phpmyadmin on the previously created network

docker run --network mydockernetwork -p <ip_address_of_instance>:8080:80 -e PMA_HOST=mysql -d phpmyadmin/phpmyadmin

```