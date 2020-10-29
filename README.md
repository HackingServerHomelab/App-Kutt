# App-Kutt

## First Time Prerequisites

1. `rm ./Data/redis/.gitkeep`
2. `rm ./Data/postgres/.gitkeep`
3. Run [Traefik](https://github.com/mattlombana/App-Traefik)

## Running the Containers

1. Update the following lines in [docker-compose.yml](./Docker/docker-compose.yml)
    * `../Data/redis:/data`
    * `../Data/postgres:/var/lib/postgresql/data`
2. Edit [postgres.env](./Docker/postgres.env)
3. Edit [kutt.env](./Docker/kutt.env)
4. Update the Traefik host label in [docker-compose.yml](./Docker/docker-compose.yml)
    * ``"traefik.http.routers.kutt.rule=Host(`localhost`)"``
3. Run `docker-compose -f ./Docker/docker-compose.yml up -d`

## First Time Setup

1. Visit <https://your-ip>
