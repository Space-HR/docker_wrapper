FROM node:18-alpine3.18 as build
WORKDIR /usr/src/app
ADD *.json ./
RUN yarn install

ADD ./public ./public
ADD ./src ./src