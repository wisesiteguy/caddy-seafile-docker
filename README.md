# Caddy-seafile-docker
1. [Install Caddy](https://caddyserver.com/docs/install)
2. Use my [Caddyfile](https://github.com/xhz8s/Caddy-seafile-docker/blob/main/Caddyfile) and replace your domain
3. "docker-compose up -d" my [docker-compose.yml](https://github.com/xhz8s/Caddy-seafile-docker/blob/main/docker-compose.yml) after changing the variables
4. Edit the file gunicorn.conf.py in the folder: "seafile-data/seafile/conf" and replace bind = "127.0.0.1:8000" with bind = "0.0.0.0:8000"
5. "docker-compose restart"
6. Done.
