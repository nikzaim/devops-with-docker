FROM node:14-alpine

WORKDIR /app

COPY . .

RUN apk update && apk add npm && npm install && npm run build && npm i -g serve

EXPOSE 5000

CMD ["npx", "serve", "-s", "-l", "5000", "build"]