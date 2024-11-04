# HomeLab Compose

This repository serves as a backup and central reference for all my Docker containers in a clear and organized Docker Compose format. It includes containers for my unRAID setup, as I don’t plan on running every container directly on unRAID in the future.

## NOTES

- Before using any of these Compose files, verify that the listed ports are free and that directory mappings are accurate. Once the configurations are set, navigate (`cd`) into the desired directory and run `docker compose up -d` to start the service. Repeat this process for any additional services you’d like to deploy.

- [Gogs](./gogs/docker-compose.yml), [Homepage](./homepage/docker-compose.yml), and [Rocket.Chat](./rocketchat/docker-compose.yml) each default to port 3000. If running multiple of these services, make sure to update the port allocations for each to avoid conflicts.

- You cannot run [LANCache](./lancache/docker-compose.yml) and [NGINX Proxy Manager](./nginxproxymanager/docker-compose.yml) both require ports 80 and 443, which prevents them from being run simultaneously on the same host. If there’s a workaround you know of, feel free to submit a PR!

- [LANCache](./lancache/docker-compose.yml) requires a .env file. I've attached the default .env file [here](./lancache/.lancache.env).

- If you’re planning to host a game server other than Minecraft, or if you’re using mods/plugins that require additional ports with [Pufferpanel](./pufferpanel/docker-compose.yml), be sure to add the necessary ports to the docker-compose.yml file.

## [TODO](./TODO.md)
