FROM ubuntu:16.04

WORKDIR /example
COPY . .

EXPOSE 5000

RUN apt-get update && apt-get -y install curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs

RUN npm run build
RUN npm install -g serve

CMD ["serve", "-s", "-l", "5000", "dist"]