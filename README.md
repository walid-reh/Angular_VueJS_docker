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

## URL to view application on browser

127.0.0.1:4200

# Vuejs template generation with Docker

## Commands

- Create image by the name of vueapp:
  docker build -t vueapp -f Dockerfile .
- Run the local docker image created:
  docker run -itd -v ${PWD}:/app --name vueapp vueapp
- Create the Vue js application :
  docker exec -it vueapp vue create my-app

docker-compose up --build

## URL to view application on browser

127.0.0.1:8080
