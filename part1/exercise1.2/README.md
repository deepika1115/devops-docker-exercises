# EXERCISE 1.2: CLEANUP

## Description

We have containers and an image that are no longer in use and are taking up space. Running docker ps -a and docker image ls will confirm this.

Clean the Docker daemon by removing all images and containers.

Submit the output for docker ps -a and docker image ls


## Solution

Solution to this exercise with successful command execution is shown in the image 'solution1.2.png'.

The commands I used are:

### To list all the containers
docker ps -a 

### To list all images
docker images

### To remove all stopped container
docker container prune

### To stop and remove one running coontainer
docker stop <container_id>
docker rm <container_id>

### Finally remove the image
docker rmi <image_id> 

### List containers and images
docker ps -a
docker images


