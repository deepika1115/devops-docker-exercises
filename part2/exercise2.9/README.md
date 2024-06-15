# EXERCISE 2.9

## Description
Most of the buttons may have stopped working in the example application. Make sure that every button for exercises works.

Remember to take a peek into the browser's developer consoles again like we did back part 1, remember also this and this.

The buttons of the Nginx exercise and the first button behave differently but you want them to match.

If you had to make any changes explain what you did and where.

Submit the docker-compose.yml and both Dockerfiles.

## Solution

The docker-compose.yml and both frontend and backend dockerfile file are added in this folder for this exercise.

Frontend Dockerfile is in the folder 'frontend-dockerfile'.
Backend Dockerfile is in the folder 'backend-dockerfile'.

### To make this working I need to update frontend and backend Envirement variable in Dockerfile.

- In frontend dockerfile upadted the following environment variable :
 
    REACT_APP_BACKEND_URL=http://localhost/api

- In backedn dockerfile upadted the following environment variable :

    REQUEST_ORIGIN=http://localhost







The screenshot of running app on http://localhost is also added in this folder.

