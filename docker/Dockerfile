FROM node:14.15.4-alpine

WORKDIR /var/www/

RUN apk update && \
    npm install && \
    npm install -g npm && \
    npm install -g vue-cli

ENV HOST 0.0.0.0
