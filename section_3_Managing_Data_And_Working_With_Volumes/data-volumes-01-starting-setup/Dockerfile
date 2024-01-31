FROM node:14

WORKDIR /app

COPY package.json .

RUN npm config set registry http://registry.npmjs.org/

RUN npm config set strict-ssl false

RUN npm install

COPY . .

EXPOSE 80

CMD [ "node", "server.js" ]