# Version basic
FROM alpine:3.10

RUN apk update && apk add nodejs-npm

WORKDIR /app

COPY . .

RUN npm install

EXPOSE 80

CMD ["npm", "start"]