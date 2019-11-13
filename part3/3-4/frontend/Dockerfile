FROM node:alpine

WORKDIR /example

COPY . .

EXPOSE 5000

RUN API_URL=http://localhost:8000 npm run build && \
    npm install -g serve

CMD ["serve", "-s", "-l", "5000", "dist"]
