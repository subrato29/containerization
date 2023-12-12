## How to run `Dockerfile`

```
Go to the directory
Run `docker build .`

```

## How many docker `running` containers available in the system

```
docker ps

`ps` stands for processes i.r. containers

```

## How many docker `running` & `non-running` containers available in the system

```
docker ps -a

```

## How to restart a docker container

```
docker restart <CONTAINER-ID>

```

## How to stop docker container

```
docker stop <CONTAINER-ID>

```

# How to start a docker container

```
docker start <CONTAINER-ID>

```

# Stop all running containers

```
docker stop $(docker ps -q)

```

# Remove all containers

```
docker rm -f $(docker ps -a -q)

```

# Remove all containers, images, networks, and volumes in one go

```
docker system prune -af

```

# How to run a docker image

```
docker run -it -d <IMAGE>
e.g. docker run -it -d ubuntu

```
