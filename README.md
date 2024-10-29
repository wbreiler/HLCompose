# HomeLab Compose

This repository is intended to have a backup, so to speak, of all my containers in an easy to read Docker Compose format. This includes containers that are running on unRAID, as I don't foresee myself running all of my containers on my unRAID host.

## NOTES

- Before using any of these Compose files, ensure you’ve checked that the specified ports are available and that directories are mapped correctly. After confirming the configuration, start the services with `docker compose up -d -f [file name(s)]`.

- Both [Gogs](./gogs.yml) and [Homepage](./homepage.yml) want port `3000`. If you decide to run both, make sure you go in and change the port allocations for one or both of them.

## [TODO](./TODO.md)
