# docker_PostgreSQL

docker-compose up -d

exec the container in interactive mode 
docker exec -it docker_postgresql_db_1 bash

launch psql with the postgres username which have the root access
psql -U postgres

\du to look for roles
we have superuser

create database btc;

\c btc

CREATE TABLE btc_usd (date TIMESTAMP, open FLOAT, high FLOAT, low FLOAT, close FLOAT, adj_close FLOAT, volume FLOAT);

btc=# COPY btc_usd FROM '/BTC-USD.csv' DELIMITER ',' CSV HEADER;