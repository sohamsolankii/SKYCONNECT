FROM node:20.19.4-alpine3.22

WORKDIR /developer/nodejs/notification-service

COPY . .

RUN npm ci

CMD ["npm","run","dev"]