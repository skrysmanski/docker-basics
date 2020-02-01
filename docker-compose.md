# docker-compose

## Basics

Start:

    docker-compose up
    docker-compose up -d

Shutdown:

    docker-compose down

## docker-compose.yml

The default name for the **compose file** is:

    docker-compose.yml

Reference: <https://docs.docker.com/compose/compose-file/>

Version Changelog: <https://docs.docker.com/compose/compose-file/compose-versioning/#version-3>

### Example

**Important:** This example file is not supposed to be working. It's just a "random" collection of useful compose directives.

```yml
version: '3.1'

services:
  wordpress:
    image: wordpress
    ports:
      # Exposes port 80 from container on 8080 on host
      # NOTE: Always use strings or the numbers will be interpreted as base 60.
      - "8080:80"
    volumes:
      # Host mounted volume
      - ./html:/var/www/html:ro
    environment:
      WORDPRESS_DB_HOST: db
      WORDPRESS_DB_USER: exampleuser

  db:
    image: mysql:5.7
    restart: always
```
