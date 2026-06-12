FROM node:22-alpine

WORKDIR /app

RUN npm install -g pm2

COPY package*.json ./

RUN npm ci

COPY . .

EXPOSE 3000

CMD ["pm2-runtime", "npm", "--", "start"]
