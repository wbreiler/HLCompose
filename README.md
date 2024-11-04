# HomeLab Compose

This repository is intended to have a backup, so to speak, of all my containers in an easy to read Docker Compose format. This includes containers that are running on unRAID, as I don't foresee myself running all of my containers on my unRAID host.

## NOTES

- Before using any of these Compose files, ensure you’ve checked that the specified ports are available and that directories are mapped correctly. After making sure the configuration(s) are correct, `cd` into the directory, then run `docker compose up -d`. Repeat for any additional services you want to run.

- Both [Gogs](./gogs/docker-compose.yml) and [Homepage](/homepage/docker-compose.yml) want port `3000`. If you decide to run both, make sure you go in and change the port allocations for one or both of them.

- You cannot run [LANCache](./lancache/docker-compose.yml) and [NGINX Proxy Manager](./nginxproxymanager/docker-compose.yml) on the same host, due to them both ~~wanting~~ needing ports `80` and `443`. If there's a way around this that I'm missing, submit a PR!

- [LANCache](./lancache/docker-compose.yml) requires a .env file. I've attached the default .env file [here](./lancache/.lancache.env).

## [TODO](./TODO.md)
