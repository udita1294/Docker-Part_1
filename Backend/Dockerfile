FROM node:22-alpine

WORKDIR /app

# COPY ./package.json ./package.json
# COPY ./index.js ./index.js
COPY . .

RUN npm install

EXPOSE 3000

CMD ["node", "index.js"]

