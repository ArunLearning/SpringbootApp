#Creation of SQLDB Container with default network
#This is before building the jar file
1. Pull the docker image
```
docker pull mysql
```
2. Create and run a container for mysql docker image
```
docker run -itd --name mysqldb --restart unless-stopped -p 3306:3306 -e MYSQL_ROOT_PASSWORD=password123 -e MYSQL_DATABASE=springboot_mysql_example mysql
```
3. To enter into a container using bash
```
docker exec -it mysqldb bash
```
4. To connect SQLDB outside container (i.e.,from host)
```
mysql --host=172.17.0.2 --port=3306 -uroot -ppassword123
```
5. verify the data base with below queries
```
show databases;
```
```
use springboot_mysql_example;
```
```
show tables; select * from product;
```
