FROM ubuntu:16.04

WORKDIR /example

COPY . .

EXPOSE 8000

RUN apt-get update && apt-get -y install curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs

RUN npm install

CMD FRONT_URL=http://localhost:5000 npm start