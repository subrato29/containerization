# Docker commands

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

## How to start a docker container

```
docker start <CONTAINER-ID>

```

## How to start a docker container in an attached mode

```
docker start -a <CONTAINER-ID OR CONTAINER-NAME>

```

## How to start a docker container in an attached and interactive mode

```
docker start -a i <CONTAINER-ID OR CONTAINER-NAME>

```

## Stop all running containers

```
docker stop $(docker ps -q)

```

## Remove all containers

```
docker rm -f $(docker ps -a -q)

```

## Remove all containers, images, networks, and volumes in one go

```
docker system prune -af

```

## How to run a docker image in interactive mode

```
docker run -it <IMAGE>
e.g. docker run -it ubuntu

```

## Deletion of a container

```
docker rm <CONTAINER_ID or CONTAINER_NAME>

```

## Deletion of an image

```
docker rmi <IMAGE_ID>

Note: If you have container that has been stopped and is used by an image, then the container needs to be removed first and then remove the the image

```

## Deletion of all unused images

```
docker image prune

```

## Deletion of a running container

```
docker stop <CONTAINER_ID or CONTAINER_NAME>
docker rm <CONTAINER_ID or CONTAINER_NAME>

```

## Forceful deletion of an image

```
First use the docker rm command to remove the stopped container.
docker rm <CONTAINER_ID OR CONTAINER_NAME>

Force deletion of image
docker rmi -f <IMAGE_ID>

```

## How to run a `Dockerfile`

```
Go to the directory where Dockerfile exist and then run below command
docker build .

And then run below command
docker run -p <LOCAL_MACHINE_PORT>:<DOCKER_CONTAINER_PORT> <IMAGE_ID>
e.g.
docker run -p 3000:80 <IMAGE_ID>

docker run -p <LOCAL_MACHINE_PORT>:<DOCKER_CONTAINER_PORT> -d <IMAGE_ID>

```

## How to run a Docker in `attach` and `detached` mode

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

## Running a docker image and once stop the container, it would automatically delete the running container

```
docker run -p <LOCAL_MACHINE_PORT>:<DOCKER_CONTAINER_PORT> -d --rm <IMAGE_ID>

Note: Need to add `--rm`


```

## How to see image details

```
docker inspect <IMAGE_ID>

```
