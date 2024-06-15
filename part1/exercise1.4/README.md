# EXERCISE 1.4: MISSING DEPENDENCIES

## Description

Start a Ubuntu image with the process sh -c 'while true; do echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website; done'

If you're on Windows, you'll want to switch the ' and " around: sh -c "while true; do echo 'Input website:'; read website; echo 'Searching..'; sleep 1; curl http://$website; done".

You will notice that a few things required for proper execution are missing. Be sure to remind yourself which flags to use so that the container actually waits for input.

Note also that curl is NOT installed in the container yet. You will have to install it from inside of the container.

Test inputting helsinki.fi into the application. It should respond with something like

<html>
  <head>
    <title>301 Moved Permanently</title>
  </head>

  <body>
    <h1>Moved Permanently</h1>
    <p>The document has moved <a href="http://www.helsinki.fi/">here</a>.</p>
  </body>
</html>

This time return the command you used to start process and the command(s) you used to fix the ensuing problems.

## Solution

### The commands I used are:

1. To start a Ubuntu image:
- $ docker run -it --name my-container ubuntu sh -c "while true; do echo 'Input website:'; read website; echo 'Searching..'; sleep 1; curl http://$website; done"

2. As the curl not found I exit my-container and start the container again and install curl by using the following commands:
- $ docker start my-container 
- $ docker exec -it my-container apt-get update
- $ docker exec -it my-container apt-get -y install curl

The successful execution of these commands are shown in the image 'solution1.4(1).png'.

3. Start the conainer again with the process in the question.
- $ docker exec -it my-container sh -c 'while true; do echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website; done'

The successfull execution of this is shown in the image 'solution1.4(2).png'.



