# ngduc/docker
Dockerfiles for lightweight dev/production images...

# Debian DEV
To get the image from Docker Hub, run:
```
docker pull ngduc/deb-dev
```

### Features
```
Debian      Jessie
NodeJS      6.2.2
Npm         3.9.5

apt-get     lsof wget unzip gawk git nano
npm -g      eslint http-server ngrok

Size        329.3 MB
```

# Debian DB

### Features
```
Debian      Jessie
MongoDB     3.4.2
CouchDB     2.0.0
```