#base image
FROM node:14 

WORKDIR /app

COPY package.json .

RUN npm config set registry http://registry.npmjs.org/

RUN npm config set strict-ssl false

RUN npm install

COPY . .

EXPOSE 3000

CMD [ "node", "app.mjs" ]