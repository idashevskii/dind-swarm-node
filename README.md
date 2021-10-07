# dind-swarm-node

How to setup Docker Swarm node using docker-in-docker container

It can be useful if you want to isolate Docker Swarm's opened ports from the host, when host is public.

See: https://hub.docker.com/_/docker


## Run DIND as Swarm node
    docker run --privileged --name dind-swarm-node -d --restart always \
      -v /path/to/dir:/mnt \
      docker:dind

## Shell into container:

    docker exec -it dind-swarm-node sh

## Setup node swarm
