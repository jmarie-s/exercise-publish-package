# Dockerfile > Docker Image > Run Docker Containers

#Test web app that returns name of host/pod/container servicing req

#Linux x64
FROM node:current-alpine

#Label container
LABEL org.opencontainers.image.title="Hello Docker Learners!" \
      org.opencontainers.image.description="Web server showing host that responded" \
      org.opencontainers.image.authors="taken from tutorial"

#Create directory in container image for app code
RUN mkdir -p /usr/src/app

#Copy app code (.) to /usr/src/app in container image
COPY . /usr/src/app

#Set working directory context
WORKDIR /usr/src/app

#Install dependencies from packages.json
RUN npm install

#Command for container to execute
ENTRYPOINT [ "node", "app.js" ]
