# EXERCISE 1.3: SECRET MESSAGE

## Description

Now that we've warmed up it's time to get inside a container while it's running!

Image devopsdockeruh/simple-web-service:ubuntu will start a container that outputs logs into a file. Go inside the running container and use tail -f ./text.log to follow the logs. Every 10 seconds the clock will send you a "secret message".

Submit the secret message and command(s) given as your answer.


## Solution

Solution to this exercise with successful command execution is shown in the image 'solution1.3.png'.

The commands I run are :

1. $ docker run -d -it --rm --name web-app devopsdockeruh/simple-web-service:ubuntu
2. $ docker exec web-app tail -f ./text.log

The secret message is: You can find the source code here: https://github.com/docker-hy
