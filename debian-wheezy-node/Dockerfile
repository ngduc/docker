FROM debian:wheezy

RUN apt-get update && apt-get install -y --no-install-recommends \
    ca-certificates \
    curl \
    build-essential \
    pkg-config \
    lsof wget unzip gawk git \
  && rm -rf /var/lib/apt/lists/*

ENV NODE_VERSION "5.5.0"

RUN curl https://nodejs.org/dist/v${NODE_VERSION}/node-v${NODE_VERSION}-linux-x64.tar.gz \
  |tar -xz -C /usr --strip-components=1

RUN npm install eslint -g
RUN npm install http-server -g
RUN npm install ngrok -g

CMD [ "node" ]