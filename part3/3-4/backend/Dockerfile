FROM node:alpine

WORKDIR /example

COPY . .

EXPOSE 8000

RUN npm install

CMD FRONT_URL=http://localhost npm start