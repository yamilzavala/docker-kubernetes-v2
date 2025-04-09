##docker run -p 3000:80 --name bind-mount-demo -d --rm -v feedback:/app/feedback -v "C:/Users/yamil.zavala/Desktop/Docker-maximilian/section-3-volumes/data-volumes-01-starting-setup:/app" -v /app/node_modules img-demo:volumes
FROM node:alpine


RUN npm install -g nodemon

WORKDIR /app

COPY package.json /app

RUN npm install

COPY . /app

ARG DEFAULT_PORT=80

ENV PORT $DEFAULT_PORT

EXPOSE $PORT

CMD ["npx", "nodemon", "--legacy-watch", "server.js"]