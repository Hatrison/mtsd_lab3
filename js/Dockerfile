FROM node:16.17.0

WORKDIR /app

COPY package*.json ./

RUN npm ci --omit=dev

COPY . .

EXPOSE 8080

CMD [ "node", "index.js" ]