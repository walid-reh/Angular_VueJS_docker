# Angular_VueJS_docker

This repo contains generated Angular and VueJS templates using Docker.

# Angular template generation

First delete the already generated files by deleting the angular-docker/app folder (we restart from scratch).

## Commands

docker-compose run app ng new angular-docker --directory . --skipInstall
uncomment the tow lines from the Dockerfile :

#COPY app/package.json ./
#RUN npm install

- Then run the following command (rebuild the containers with our new commands):

docker-compose up --build

- In order to relaunch the application on the container use the command :

docker-compose up

# URL to view application on browser

127.0.0.1:4200
