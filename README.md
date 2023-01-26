# Caddy-seafile-docker
1. [Install Caddy](https://caddyserver.com/docs/install)
2. Use my [Caddyfile](https://github.com/xhz8s/Caddy-seafile-docker/blob/main/Caddyfile) and replace example.com with your domain
3. Use my [docker-compose.yml](https://github.com/xhz8s/Caddy-seafile-docker/blob/main/docker-compose.yml) to set up seafile-docker and adjust the variables marked with "<>". You can use the offical [documentation](https://manual.seafile.com/docker/deploy_seafile_with_docker/) for help
4. Let Seafile build itself "docker-compose up -d"
5. Edit the file gunicorn.conf.py in the folder: "seafile-data/seafile/conf" and replace bind = "127.0.0.1:8000" with bind = "0.0.0.0:8000"
6. "docker-compose restart"
7. Done.
