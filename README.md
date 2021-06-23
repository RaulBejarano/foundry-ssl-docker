# Foundry VTT with SSL (HTTPS) using Docker Compose

This is a configuration project to have Foundry VTT behind a Nginx reverse proxy that handles SSL using Let's Encrypt.

## Requirements

- [Docker](https://docs.docker.com/get-docker/)
- [Docker-compose](https://docs.docker.com/compose/install/)

## Installation
1. Download this repo: `git clone git@github.com:RaulBejarano/docker-compose-foundryvtt-certbot.git`
2. Modify the files 
   - `proxy/init-letsencrypt.sh`: look for `<YOUR DOMAIN HERE>` and `<YOUR EMAIL HERE>` and change them for your domain and email. This will configure SSL .
   - `proxy/nginx/app.conf`: look for `<YOUR DOMAIN HERE>` and change it for your domain (4 times). This will configure the reverse proxy.
   - `docker-compose.yml`: look for `<YOUR FOUNDRY PASSWORD HERE>`, `<YOUR FOUNDRY USERNAME HERE>`, `<YOUR FOUNDRY SERVER ADMIN PASSWORD HERE>`, `<YOUR FOUNDRY LICENSE KEY HERE>` and chage it with your own variables.
3. Execute `init-letsencrypt.sh` in its directory.
4. Execute `docker-compose up` in `docker-compose.yml` directory.

