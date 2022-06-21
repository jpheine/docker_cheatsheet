# Docker Cheatsheet

## Containers

### Docker Container run
Run a container:
-p run in Background
--name specify container name
--rm delete container after running

`docker container run (-d --name --rm) containername containerimage`

-t psuedo-TTY (prompt)
-i interactive
Add shelltype or program at the end

`docker container run -it --name containername containerimage programname`

-p expose port
`docker container -p hostport:containerport --name containername -d containerimage 

Connect container to network (add at end):

`network networkname`

### Docker container stop
`docker container stop containername`

### Docker container ls
Show all running containers and basic stats

`docker container ls`

Show all (also stopped) containers and basic stats

`docker container ls -a`

### Docker container start
Start (rerun) a container

`docker container start containername`

-a attach
-i interactive

`docker container start -ai containername`

### Docker container exec
`docker container exec -it containername programname`

example (run bash in mysql)

`docker container exec -it mysql bash`

### docker container inspect
Get detailed info about container

`docker container inspect containername`

### docker container port
Show exposed ports

`docker container port containername`

### docker network ls
Show networks

`docker network ls`

Show details

`docker network inspect`

Attach container

`docker network connect`
`docker netowrk disconnect`

Example: 

`docker network connect networkname containername`

Create network

`docker network create networkname`

## Images

### docker pull
pull latest image:

`docker pull imagename`

### docker image ls
Overview of all images:

`docker image ls` 

### docker image inspect

Get detailed information about image:
`docker image inspect imagename`

### docker image history
Show image layers:

`docker image history imagename`

## Docker Tag
Retag an existing image (e.g. for push)

Attention: Multiple Tags can be used for the Same image. Image ID unqiuely identifies the image.

`docker tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG]`

## Dockerfile
Runned top down -> order matters.

`FROM` required

`ENV` importand -> Set environment variables

`RUN` optional commands to run at shell in container at build time

`Expose` expose ports

`CMD` run whenever container is launched

## Volumes
Have to be manually deleted! Survive deletion of container!

Show all volumes:

`docker volume ls`

Inspect volumne:

`docker volume ls volumeid`

Name for volume, In docker container run:

-v mysql-db:/var/... 
