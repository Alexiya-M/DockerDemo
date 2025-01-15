FROM node:18-alpine

WORKDIR /usr/src/app

COPY src/practicum/package*.json ./
RUN npm install

COPY src/practicum/ ./

RUN npm run build

FROM node:18-alpine AS practicum

COPY --frontbuilder /app/.next ./. next
COPY --frontbuilder /app/package.json ./package.json

RUN npm-install --practicum

EXPOSE 3000
ENV NODE_ENV production

CMD ("npm", "start")
