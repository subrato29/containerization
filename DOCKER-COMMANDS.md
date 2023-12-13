## How to run `Dockerfile`

```
Go to the directory
Run `docker build .`

```

## How many docker `running` containers available in the system

```
docker ps

`ps` stands for processes i.e. containers

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

# Deletion of an image

```
docker rmi <image_id>

```

# Forceful deletion of an image

```
First use the docker rm command to remove the stopped container.
docker rm <CONTAINER_ID>

Force deletion of image
docker rmi -f <IMAGE_ID>

```

# How to run a `Dockerfile`

```
Go to the directory where Dockerfile exist and then run below command
docker build .

And then run below command
docker run -p <LOCAL_MACHINE_PORT>:<DOCKER_CONTAINER_PORT> <IMAGE_ID>
e.g.
docker run -p 3000:80 <IMAGE_ID>

docker run -p <LOCAL_MACHINE_PORT>:<DOCKER_CONTAINER_PORT> -d <IMAGE_ID>

```

# How to run a Docker in `attach` and `detached` mode

```
- attach mode
docker run -p <LOCAL_MACHINE_PORT>:<DOCKER_CONTAINER_PORT> <IMAGE_ID>
e.g.
docker run -p 3000:80 <IMAGE_ID>

OR
docker attach <NAME OR CONTAINER-ID>

OR
docker start -a <NAME OR CONTAINER-ID>

- detached mode
docker run -p <LOCAL_MACHINE_PORT>:<DOCKER_CONTAINER_PORT> -d <IMAGE_ID> (mention -d)
e.g.
docker run -p 3000:80 -d <IMAGE_ID>


```

## To show all docker images

```
docker images

```
