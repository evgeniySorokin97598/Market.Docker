
FROM node:latest as build
EXPOSE 81
EXPOSE 443


FROM node:latest as build
WORKDIR /app

RUN npm install -g @angular/cli

COPY ./package.json .
RUN npm install
COPY app .
FROM nginx as runtime
COPY  app /usr/share/nginx/html
COPY nginx.conf /etc/nginx/nginx.conf



