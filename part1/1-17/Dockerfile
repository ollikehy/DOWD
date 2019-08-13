FROM ubuntu:16.04

WORKDIR /environment

RUN apt-get update && apt-get -y install curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs

ENTRYPOINT /bin/bash

# Ubuntu with Node installed