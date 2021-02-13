# App-Homer

## First Time Prerequisites

1. Configure the [config.yml](./Config/config.yml) file
2. Run [Traefik](https://github.com/HackingServerHomelab/App-Traefik)

## Running the Containers

1. Configure the following mount points in [docker-compose.yml](./Docker/docker-compose.yml)
    * `../Data/assets:/www/assets`
    * `../Config/config.yml:/www/assets/config.yml`
3. Update the Traefik host label in [docker-compose.yml](./Docker/docker-compose.yml)
    * ``"traefik.http.routers.homer.rule=Host(`localhost`)"``
4. Run `docker-compose -f ./Docker/docker-compose.yml up -d`

## First Time Setup

1. Visit <https://your-ip>
