# 6_BDI_8apr_StorageII_Assignment

Run container:

    docker run -dit -v $(pwd)/sql_scripts:/sql_scripts postgres:latest

Exec Postgres Shell and create database:

    docker exec -it <ID_CONTAINER> psql -U postgres
    psql (11.2 (Debian 11.2-1.pgdg90+1))
    Type "help" for help.

    postgres=# create database hospital;
    CREATE DATABASE

Create tables in our database:

    docker exec -it <ID_CONTAINER> psql -U postgres -d hospital -f /sql_scripts/script.sql

Insert data in our database:

    docker exec -it <ID_CONTAINER> psql -U postgres -d hospital -f /sql_scripts/insert_script.sql
