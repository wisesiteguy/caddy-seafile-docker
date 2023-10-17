# caddy-seafile-docker
1. [install Caddy](https://caddyserver.com/docs/install)
2. use my [Caddyfile](https://github.com/xhz8s/Caddy-seafile-docker/blob/main/Caddyfile) and replace example.com with your domain
3. use my [docker-compose.yml](https://github.com/xhz8s/Caddy-seafile-docker/blob/main/docker-compose.yml) to set up seafile-docker and adjust the variables marked with "<>". You can use the offical [documentation](https://manual.seafile.com/docker/deploy_seafile_with_docker/) for help
4. let Seafile build itself "docker-compose up -d"
5. edit the file gunicorn.conf.py in the folder: "seafile-data/seafile/conf" and replace bind = "127.0.0.1:8000" with bind = "0.0.0.0:8000"
6. restart seafile-docker "docker-compose restart"
7. Once running, in the admin settings, make sure FILE_SERVER_ROOT has 'httpS' added, otherwise the network will fail
8. Done.
