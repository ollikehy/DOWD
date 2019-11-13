FROM ubuntu:16.04

WORKDIR /example

COPY . .

EXPOSE 5000

RUN apt-get update && apt-get -y install curl && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt install -y nodejs && \
    npm run build && \
    npm install -g serve && \
    apt-get purge -y --auto-remove curl && \
    rm -rf /var/lib/apt/lists/* &&\
    useradd -m app &&\
    chown app /example

USER app

CMD ["serve", "-s", "-l", "5000", "dist"]