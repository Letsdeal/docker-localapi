FROM node:6.9.2

RUN apt-get update && apt-get install -y \
    git \
 && rm -rf /var/lib/apt/lists/*

RUN npm install -g localapi@1.6.0 \
 && npm cache clean

RUN mkdir -p /data
VOLUME /data
WORKDIR /data

EXPOSE 3333

ENTRYPOINT ["localapi"]

CMD ["--help"]
