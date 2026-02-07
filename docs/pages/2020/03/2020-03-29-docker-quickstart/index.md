---
title: "docker quickstart"
date: 2020-03-29
categories: 
  - "vizz"
tags: 
  - "containers"
  - "docker"
  - "images"
---

docker quickstart

```
# aptitude install docker.io

# systemctl enable docker
# systemctl start docker
# systemctl is-active docker.service
# systemctl status docker.service

# usermod -aG docker $USER
```

logout of xwindows

login to xwindows

git clone & docker build

```
$ git clone my-image 
$ docker build my-image
```

docker pull

```
$ docker pull infrabuilder/foldingathome
```

docker run and monitor

```
$ docker run -d --name humpty-dumpty hello-world
$ docker ps [to confirm container name ie humpty-dumpty]
$ docker logs -f humpty-dumpty
$ docker top humpty-dumpty
$ docker stop humpty-dumpty
$ docker kill humpty-dumpty
```

manage docker containers

```
$ docker stats
$ docker ps
$ docker ps -a$ docker rm humpty-dumpty
```

manage docker images

```
$ docker images
$ docker rmi hello-world
```

docs

- https://docs.docker.com/engine/docker-overview/
- https://docs.docker.com/install/linux/linux-postinstall/
- https://docs.docker.com/get-started/
- https://docs.docker.com/get-started/part2/
