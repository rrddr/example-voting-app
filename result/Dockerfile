FROM node:8.9-alpine

WORKDIR /app

COPY . .

RUN npm install -g nodemon
RUN npm config set registry https://registry.npmjs.org
RUN npm install
RUN npm ls
RUN npm cache clean --force
RUN  mv /app/node_modules /node_modules

EXPOSE 80

CMD ["node", "server.js"]
