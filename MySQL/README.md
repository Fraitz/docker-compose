## What you'll find here?

This is a simple document for you to create a container with MySQL Server;

With this doc. you can dockerize MySQL application to use in projects without having to install MySQL in your machine. 

> To use this doc, simply go to the folder where you whant to create it in your machine:
>
>Recomended: `home -> dockerComposes -> MySQL`
>
>


Open your terminal and type:

```
docker-compose up
```

To use MySQL inside your container, open your terminal (host) and type:
```
docker exec -it MySQL_Container bash
```
And, inside the container terminal, type:
```
mysql -u root -proot
```

In case you have the MySQL server installed in host, you cant run the following command in terminal:
```
mysql -u root -proot -h 0.0.0.0
```

>To install a database schema in your dockerized `MySQL Server`, download the `schema.sql file` to MySQL container volume, open the container terminal, go to a folder where you have a database schema `.sql` file and type the following:
```
 mysql -u root -proot -h 0.0.0.0 < schemaName.sql 
```
If you have the `MySQL Server` installed in your host, you can download the `schema.sql` in whatever folder you want, and just run the cli comand above int this folder.

The `docker-compose.yml` file used in this folder was picked from [this repo](https://github.com/RoyMusthang/docker-compose/tree/master/mysql)!