[![SSL Report](https://img.shields.io/badge/SSL%20Report-A-brightgreen)](https://www.ssllabs.com/ssltest)
[![TLS Version](https://img.shields.io/badge/TLS-v1.3-blue)](#)
[![Platform](https://img.shields.io/badge/platform-linux%20|%20macos%20|%20windows-lightgrey)](#)

# ghost-sqlite-compose
easy [Ghost](https://ghost.org/) self-hosting with docker-compose

#### Prerequisites

You will need [docker](https://docs.docker.com/engine/install/) and [docker-compose](https://docs.docker.com/compose/install/compose-plugin/)

For running this configuration you will need a machine with 512MB of RAM. If your blog has estimate of less than 100K hits/day you will be fine with sqlite, but with heavier load consider using [ghost-mysql-compose](https://github.com/linnik/ghost-mysql-compose).

#### SSL

SSL Certificate will be generated and refreshed automatically by `Traefik`. You only need to specify your domain and mail address for ACME notifications in a config file `.env`.

#### Setup

1. Clone this repo and create default config from template

```bash
git clone https://github.com/linnik/ghost-sqlite-compose.git
cd ghost-sqlite-compose
cp env.template .env
```

2. Replace default values in a config file named `.env`. Leave no empty values!

3. Launch

```bash
docker compose up -d
docker compose ps
```
