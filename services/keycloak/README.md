# Keycloak

## Sobre

**Keycloak** an Open Source Identity and Access Management.

> [`www.keycloak.org`](https://www.keycloak.org/)

Add authentication to applications and secure services with minimum effort. No need to deal with storing users or authenticating users.

## Keycloak em container Docker

```sh
# criar rede
docker network create service_net

# docker run
docker run -d --rm \
  --name keycloak \
  --network service_net \
  -e KC_BOOTSTRAP_ADMIN_USERNAME=admin \
  -e KC_BOOTSTRAP_ADMIN_PASSWORD=changeit123! \
  -p 8080:8080 \
  quay.io/keycloak/keycloak:26.3.4 start-dev

# limpar
docker stop keycloak
docker network rm service_net
```

## Versão Docker Compose

### Instância simples em modo `start-dev`

- [`keycloak-v01.yaml`](./keycloakv-01.yaml)

```sh
# docker compose
docker compose -f keycloak-v01.yaml up -d

# verificando
docker compose -f keycloak-v01.yaml ls
docker compose -f keycloak-v01.yaml ps

# limpar
docker compose -f keycloak-v01.yaml down -v
```

### Usando um PostgreSQL

- [`keycloak-v02.yaml`](./keycloak-v02.yaml)

```sh
# docker compose
docker compose -f keycloak-v02.yaml up -d

# verificando
docker compose -f keycloak-v02.yaml ls
docker compose -f keycloak-v02.yaml ps

# limpar
docker compose -f keycloak-v02.yaml down -v
```

## Por enquanto

...é isso pessoal!!!
