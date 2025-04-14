# (build image)   1. docker build -t node-dep-example .
# (build image)   2. docker tag node-dep-example yamil189/node-example-1
# (build image)   3. docker push yamil189/node-example-1
# (run container) 4. docker run -d --rm -p 80:80 --name node-dep node-dep-example

FROM node:14-alpine

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

CMD ["node", "app.js"]