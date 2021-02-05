FROM node:14.15.4-alpine

WORKDIR /var/www/

RUN apk update && \
    apk add wget && \
    mkdir /.nvm && \
    npm install && \
    npm install -g npm && \
    npm install -g vue-cli

COPY ./nvm/ /.nvm

RUN chmod 777 -R /.nvm/ && \
    . /.nvm/nvm.sh && \
    nvm install v14.15.4

ENV HOST 0.0.0.0
