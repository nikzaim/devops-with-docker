FROM node:18-alpine

RUN apk add --no-cache git

WORKDIR /app

RUN git clone https://github.com/nikzaim/react-image-slider.git .

RUN yarn install

EXPOSE 4173

RUN yarn build

CMD ["yarn", "preview", "--host", "0.0.0.0"]
