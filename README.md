#Updated mariadb 10.1 server based on debian 9

https://github.com/PalinuroSec/pserver-mariadb


# Run

 docker run --name <instance_name> -v <db_name>:/var/lib/mysql --env MYSQL_ROOT_PASSWORD=<root_password> pserver/mariadb:<version>

example:
 docker run --name database1 -v mydatabase:/var/lib/mysql --env MYSQL_ROOT_PASSWORD=suca pserver/mariadb:latest


# Build
git pull https://github.com/PalinuroSec/pserver-mariadb
cd pserver-mariadb
docker build -t mariadb:<version> .
