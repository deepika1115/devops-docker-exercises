FROM node:16-slim

WORKDIR /usr/src/app

COPY . .

RUN npm install

# Set environment variable
ENV REACT_APP_BACKEND_URL=http://localhost/api

RUN REACT_APP_BACKEND_URL=http://localhost/api npm run build

COPY build* ./

RUN npm install -g serve

# EXPOSE 5000

CMD [ "serve", "-s", "-l", "5000", "build" ]

