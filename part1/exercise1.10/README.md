# EXERCISE 1.10: PORTS OPEN

## Description

In this exercise, we won't create a new Dockerfile.

The image devopsdockeruh/simple-web-service will start a web service in port 8080 when given the argument "server". In Exercise 1.8 you already did an image that can be used to run the web service without any argument.

Use now the -p flag to access the contents with your browser. The output to your browser should be something like: { message: "You connected to the following path: ...

Submit your used commands for this exercise.

## Solution

The command I used to complete this exercise is:

$ docker run -p 127.0.0.1:3000:8080 web-server

The screenshot of the command run in terminal is added in this folder named as 'command.png'.

The screenshot of the app running on localhost is added in the 'localhost.png'.



