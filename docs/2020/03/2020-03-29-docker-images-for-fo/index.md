---
title: "docker images for @foldingathome"
date: 2020-03-29
categories: 
  - "vizz"
tags: 
  - "docker"
  - "folding"
  - "foldingathome"
---

docker images for @foldingathome

- https://hub.docker.com/search?q=foldingathome&type=image

today there were ~ 30 images to choose from including

- https://hub.docker.com/r/infrabuilder/foldingathome
- https://hub.docker.com/r/linuxserver/foldingathome
- https://hub.docker.com/r/osde8info/foldingathome
- https://hub.docker.com/r/robertnetz/foldingathome

on github

- https://github.com/InfraBuilder/docker-foldingathome
- https://github.com/osde8info/docker-foldingathome
- https://github.com/linuxserver/docker-foldingathome
- https://github.com/robertnetz/foldingathome

vendors

- https://infrabuilder.com/
- http://osde.info
- https://www.linuxserver.io/
- https://netzschwitz.de/

docker pull & run cmds

```
$ docker pull infrabuilder/foldingathome
$ docker run -d \
-e USER="*MYUSER*" -e PASSKEY="*MYPASSKEY*" -e TEAM="236450" \
-e CPUS=2 \
--name folding infrabuilder/foldingathome

$ docker pull osde8info/foldingathome \
$ docker run -d \
-e USER="*MYUSER*" -e PASSKEY="*MYPASSKEY*" -e TEAM="236450" \
-e CPUS=2 \ 
--name folding osde8info/foldingathome

```
