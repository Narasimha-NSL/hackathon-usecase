FROM node:18

WORKDIR /app

COPY application-service/package*.json ./

RUN npm install

COPY application-service/. .

EXPOSE 3000

CMD ["node", "index.js"]

