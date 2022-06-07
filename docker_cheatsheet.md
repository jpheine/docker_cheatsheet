# Docker Cheatsheet

## Docker Container run
Run a container:
-p run in Background
--name specify container name
`docker container run -d --name containername containerimage`

-t psuedo-TTY (prompt)
-i interactive
Add shelltype or program at the end
`docker container run -it --name containername containerimage programname`

-p expose port
`docker container -p hostport:containerport --name containername -d containerimage 

Connect container to network (add at end):
`network networkname`

## Docker container stop
`docker container stop containername`

## Docker container ls
Show all running containers and basic stats
`docker container ls`

Show all (also stopped) containers and basic stats
`docker container ls -a`

## Docker container start
Start (rerun) a container
`docker container start containername`

-a attach
-i interactive
`docker container start -ai containername`

## Docker container exec
`docker container exec -it containername programname`

example (run bash in mysql)
`docker container exec -it mysql bash`

## docker pull
pull latest image:
`docker pull imagename`

## docker image ls
Overview of all images:
`docker image ls` 

## docker container inspect
Get detailed info about container
`docker container inspect containername'

## docker container port
Show exposed ports
`docker container port containername`

## docker network ls
Show networks
`docker network ls`

Show details
`docker network inspect`

Attach container
`docker network connect`
`docker netowrk disconnect`
Example: `docker network connect networkname containername`

Create network
`docker network create networkname`

