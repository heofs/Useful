# Docker

* `docker ps -a` - Show all containers
* `docker ps` - Show all running containers
* `docker images` - Show all images
* `docker start CONTAINERID` - Start container with id
* `docker stop CONTAINERID` - Stop container with id
* `docker image rm IMAGEID`  - Remove docker image with id
* `docker container rm CONTAINERID` - Remove docker container with id
* `docker volumes ls` - Show all volumes
* `docker volumes prune` - Remove all unused volumes
* `docker network ls` - Show docker network connections

## MongoDB Container

* `docker run --name some-mongo -d mongo:4.0.5` - Create container with 
* `docker exec -it some-mongo bash` - Access the container terminal
* `mongo` - Starts mongo terminal

## PostgreSQL Container

* `docker pull postgres`
* `docker run --name some-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgres`
* `docker run -d -p 5432:5432 --name my-postgres -e POSTGRES_PASSWORD=mysecretpassword postgres`
* `docker exec -it my-postgres bash`
* `psql -h localhost -p 5432 -U postgres -W`

## Run Docker commands without sudo

1. Add the `docker` group if it doesn't already exist

```console
$ sudo groupadd docker
```

2. Add the connected user `$USER` to the docker group
```console
$ sudo gpasswd -a $USER docker
```

3. Restart the `docker` daemon
```console
$ sudo service docker restart
```
