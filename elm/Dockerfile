# FROM node:9.11-alpine
# FROM node:10.8
FROM node:13.3-alpine3.10

MAINTAINER Hamilton

# RUN apt-get update

# RUN apt-get -y install nodejs-legacy

RUN npm config set unsafe-perm=true

RUN npm install -g elm

ENTRYPOINT ["elm"]
