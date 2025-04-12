# (build image)   1. docker build -t node-dep-example .
# (run container) 2. docker run -d --rm -p 80:80 --name node-dep node-dep-example

FROM node:14-alpine

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

CMD ["node", "app.js"]