FROM ubuntu:16.04

WORKDIR /temp
RUN apt-get update && apt-get -y install curl
COPY curler.sh .

CMD ["/bin/bash", "./curler.sh"]