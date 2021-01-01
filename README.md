# ngduc/docker
Dockerfiles for lightweight dev/production images...

# Debian DEV
To get the image from Docker Hub, run:
```
docker pull ngduc/node
```

### Features

Debian - Buster

```
NodeJS      15.5.0
Npm         TBD

apt-get     git lsof curl wget zip unzip gawk nano bc htop sed gawk
npm -g      yarn create-react-app ts-node serve ngrok

size        TBD
```

Jessie

```
Debian      Jessie
NodeJS      6.2.2
Npm         3.9.5

apt-get     lsof wget unzip gawk git nano
npm -g      eslint http-server ngrok

size        329.3 MB
```

# Debian DB

### Features
```
Debian      Jessie
MongoDB     3.4.2
CouchDB     2.0.0
```

# Common

```
docker stop $(docker ps -a -q)
docker ps

docker rmi $(docker images -q)
docker images
```