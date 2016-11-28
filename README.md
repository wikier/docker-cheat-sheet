# My personal Docker cheat sheet

Docker Engine is [plenty of commands](https://docs.docker.com/engine/reference/commandline/). 
There are more detailed cheat sheets out there (e.g., [this one](https://github.com/wsargent/docker-cheat-sheet));
here I just try to put together some useful commands/tips I usually need.

## List running containers

    docker ps

(appending `-a` lists all)

## Commit current version of the container

    docker commit CONTAINER_ID pipeline

## Stop a container

    docker stop CONTAINER_ID

## Remove a container

    docker rm CONTAINER_ID

## Remove all containers

    docker rm $(docker ps -a -q)

## List images

    docker images --tree

## Remove an image

    docker rmi IMAGE_ID

## Remove non-labelled images

    docker rmi $(docker images -q --filter "dangling=true")

## Remove all images

    docker rmi $(docker images -q)`
