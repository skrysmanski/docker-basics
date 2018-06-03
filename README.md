# Docker Cheat Sheet

## Running Containers
Run container in *foreground*:

    docker run --rm -ti <imagename>

Run container in *background*:

    docker run --rm -d <imagename>

Port mapping:

    docker run -p <host_port>:<container_port> ...

Container name:

    docker run --name <containername> ...


## Building Images
Build container:

    docker build --tag <imagename> .


## Listing Things

All images:

    docker images

All running containers:

    docker ps

All containers (including stopped):

    docker ps -a
