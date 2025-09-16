# Postgres

## Sobre

### PostgreSQL

The World's Most Advanced Open Source Relational Database.

> [`https://www.postgresql.org/`](https://www.postgresql.org/)
>
> [Docker Hub: postgres](https://hub.docker.com/_/postgres)

**PostgreSQL** is a powerful, open source object-relational database system with over 35 years of active development that has earned it a strong reputation for reliability, feature robustness, and performance.

### pgAdmin

**pgAdmin** is the most popular and feature rich Open Source administration and development platform for PostgreSQL, the most advanced Open Source database in the world.

> [`https://www.pgadmin.org/`](https://www.pgadmin.org/)
> 
> [Docker Hub: dpage/admin4](https://hub.docker.com/r/dpage/pgadmin4)

pgAdmin is a free software project released under the [PostgreSQL licence](https://www.pgadmin.org/licence/). The software is available in source and binary format from the [PostgreSQL mirror network](https://www.postgresql.org/ftp/pgadmin/).

## Postgres em container Docker

```sh
# criar volume
docker volume create postgres_data

# criar rede
docker network create service_net

# docker run
docker run -d --rm \
  --name postgres \
  --network service_net \
  -e POSTGRES_DB=mydatabase \
  -e POSTGRES_USER=admin \
  -e POSTGRES_PASSWORD=changeit123! \
  -p 5432:5432 \
  -v postgres_data:/var/lib/postgresql/data \
  postgres:17

# limpar
docker stop postgres
docker network rm service_net
docker volume rm postgres_data
```

## pgAdmin

```sh
# criar rede
docker network create service_net

# docker run
docker run -d --rm \
  --name pgadmin \
  --network service_net \
  -e PGADMIN_DEFAULT_EMAIL=admin@pgadmin.edu \
  -e PGADMIN_DEFAULT_PASSWORD=changeit123! \
  -p 8432:80 \
  dpage/pgadmin4:9.8.0

# limpar
docker stop pgadmin
docker network rm service_net
```

## Versão Docker Compose (01)

- [`postgresv01-compose.yaml`](./postgresv01-compose.yaml)

```sh
# criar rede
docker network create service_net

# docker compose
docker compose -f postgresv01-compose.yaml up -d

# verificando
docker compose -f postgresv01-compose.yaml ls
docker compose -f postgresv01-compose.yaml ps

# limpar
docker compose -f postgresv01-compose.yaml down -v
```
