# image: docker build -t goals-node .
# container: docker run --name goals-backend --rm -p 80:80 --network goals-net -v "$PWD:/app" -v /app/node_modules -v logs:/app/logs -e CHOKIDAR_USEPOLLING=true \ goals-node

FROM node

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

ENV MONGODB_USERNAME=root
ENV MONGODB_PASSWORD=secret

CMD ["npm", "start"]