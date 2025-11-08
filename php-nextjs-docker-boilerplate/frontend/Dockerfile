FROM node:18

WORKDIR /app

COPY package*.json ./
RUN npm install

# Do not build — dev server will do live reload

CMD ["npm", "run", "dev"]
EXPOSE 3000
