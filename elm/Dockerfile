FROM node:13.8-alpine3.10

MAINTAINER Hamilton

# RUN apt-get update

# RUN apt-get -y install nodejs-legacy

RUN npm config set unsafe-perm=true

RUN npm install -g elm

ENTRYPOINT ["elm"]
