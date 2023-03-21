
# Main


## Create a docker network with mysql and phpadmin.

```
docker network create mydockernetwork

docker run --network mydockernetwork -e MYSQL_ROOT_PASSWORD=my-secret-password --name mysql -d mysql:latest

docker run --network mydockernetwork -p <ip_address_of_instance>:8080:80 -e PMA_HOST=mysql -d phpmyadmin/phpmyadmin
```
