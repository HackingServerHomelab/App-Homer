# App-Homer

## First Time Prerequisites

1. Configure the [config.yml](./Config/config.yml) file

## Running the Containers

1. Run `./Config/gen_certs.sh` to generate the SSL certificates (alternatively,
   add custom certs to the private folder)
2. Update the `server_name` in [nginx.conf](./Config/nginx.conf)
3. Configure the following mount points in [docker-compose.yml](./Docker/docker-compose.yml)
    * `../Data/assets:/www/assets`
    * `../Config/config.yml:/www/assets/config.yml`
4. Run `docker-compose -f ./Docker/docker-compose.yml up -d`

## First Time Setup

1. Visit <https://your-ip>
