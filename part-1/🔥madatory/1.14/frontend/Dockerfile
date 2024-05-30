FROM node:14-alpine

WORKDIR /app

COPY . .

ENV REACT_APP_BACKEND_URL=http://localhost:8080

RUN apk update && apk add npm && npm install && npm run build && npm i -g serve

EXPOSE 5000

CMD ["npx", "serve", "-s", "-l", "5000", "build"]