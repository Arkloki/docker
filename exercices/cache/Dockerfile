# dockerfile avancé , dependance déja integrée
FROM node:12.13-alpine

WORKDIR /app

COPY . .

RUN npm install

EXPOSE 80

CMD ["npm", "start"]