FROM debian:jessie

RUN apt-get update && apt-get install -y --no-install-recommends \
    ca-certificates \
    build-essential \
    pkg-config \
    lsof curl wget unzip gawk git nano \
  && rm -rf /var/lib/apt/lists/*

ENV NODE_VERSION "6.2.2"

RUN curl https://nodejs.org/dist/v${NODE_VERSION}/node-v${NODE_VERSION}-linux-x64.tar.gz \
  |tar -xz -C /usr --strip-components=1

RUN npm install eslint -g
RUN npm install http-server -g
RUN npm install ngrok -g

CMD [ "node" ]
