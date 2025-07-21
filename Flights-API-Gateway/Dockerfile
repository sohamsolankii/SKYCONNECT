FROM node:20.19.4-alpine3.22

WORKDIR /developer/nodejs/Api-Gateway

COPY . .

RUN npm ci

CMD ["npm","run","dev"]