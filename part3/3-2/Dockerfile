FROM ubuntu:latest

RUN apt-get update && \
    apt-get install -y python3-pip && \
    apt-get install -y ffmpeg && \
    apt-get install -y wget && \
    cd /usr/local/bin &&\
    ln -s /usr/bin/python3 python && \
    pip3 install --upgrade pip yle-dl pycryptodome && \
    rm -rf /var/lib/apt/lists/*


WORKDIR /app

ENTRYPOINT ["yle-dl"]