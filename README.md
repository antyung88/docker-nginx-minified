# docker-nginx-minified

Docker Slim Build in Github Actions 6.91MB

```
REPOSITORY                     TAG       IMAGE ID       CREATED         SIZE
ghcr.io/antyung88/nginx.slim   latest    fe61b14cf63d   1 minutes ago   6.91MB
nginx                          latest    de2543b9436b   1 minutes ago   142MB
```

```
CONTAINER ID   IMAGE                          COMMAND                  CREATED          STATUS          PORTS     NAMES
98650b0e8f8a   ghcr.io/antyung88/nginx.slim   "/docker-entrypoint.…"   60 seconds ago   Up 60 seconds   80/tcp    nginx.slim
```

nginx.conf

```                                                
version: '3'
services:
  nginx:
    image: ghcr.io/antyung88/nginx.slim:latest
    volumes:
      - ./nginx:/etc/nginx/conf.d
      - ./data/html:/var/www/html
    ports:
      - 80:80
```
