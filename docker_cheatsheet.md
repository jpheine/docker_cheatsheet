# Docker Cheatsheet

## Docker Container run
Run a container:
-p run in Background
--name specify container name
docker container run -d --name containername containerimage

-t psuedo-TTY (prompt)
-i interactive
Add shelltype or program at the end
docker container run -it --name containername containerimage programname

## Docker container stop
docker container stop containername

## Docker container ls
Show all running containers and basic stats
docker container ls

Show all (also stopped) containers and basic stats
docker container ls -a

## Docker container start
Start (rerun) a container
docker container start containername

-a attach
-i interactive
docker container start -ai containername

## Docker container exec
docker container exec -it containername programname

example (run bash in mysql)
docker container exec -it mysql bash

## docker pull
pull latest image:
docker pull imagename

## docker image ls
Overview of all images:
docker image ls 
