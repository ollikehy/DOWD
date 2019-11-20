FROM ubuntu:16.04 AS build-stage

WORKDIR /example

COPY . .

RUN apt-get update && apt-get -y install curl &&\
    curl -sL https://deb.nodesource.com/setup_10.x | bash &&\
    apt install -y nodejs && \
    npm install -g serve && \
    npm run build

FROM node

EXPOSE 5000

WORKDIR /example

RUN npm install -g serve

COPY --from=build-stage /example/dist /example/dist

CMD ["serve", "-s", "-l", "5000", "dist"]
