FROM node:20.19.4-alpine3.22

WORKDIR /developer/nodejs/flight-booking

COPY . .

RUN npm ci

CMD ["npm","run","dev"]