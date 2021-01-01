# 2021-01-01 - r001

# BUILD:  docker build -t ngduc/node .
# USAGE:  use "docker-compose.yml" and run:   docker-compose run --rm web 

FROM node:15.5-buster

# Specify the absolute path to the repository mount point in an environment variable (so it can be changed). Defaults to "/app"
WORKDIR /work

RUN apt-get update && apt-get install -y --no-install-recommends \
    ca-certificates \
    build-essential \
    pkg-config \
    git \
    lsof curl wget zip unzip gawk nano bc htop sed gawk \
  && rm -rf /var/lib/apt/lists/*

RUN npm install create-react-app -g
RUN npm install ts-node -g
RUN npm install serve -g
RUN npm install ngrok -g

COPY init.sh /opt/

# ENTRYPOINT ["/opt/init.sh"]

CMD ["/opt/init.sh"]