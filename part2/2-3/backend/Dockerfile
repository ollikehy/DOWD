FROM ubuntu:16.04

WORKDIR /app

COPY . .

EXPOSE 8000

RUN apt-get update && apt-get -y install curl && \ 
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt install -y nodejs && \
    npm install && \
    apt-get purge -y --auto-remove curl && \
    rm -rf /var/lib/apt/lists/*

CMD ["npm", "start"]