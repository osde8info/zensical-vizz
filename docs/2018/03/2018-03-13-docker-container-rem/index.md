---
title: "docker container removal"
date: 2018-03-13
categories: 
  - "vizz"
tags: 
  - "container"
  - "delete"
  - "docker"
  - "removal"
---

docker container removal

```
$ docker container list --all
CONTAINER ID IMAGE COMMAND CREATED STATUS PORTS NAMES
7892a81691c6 docker/ucp "/bin/ucp-tool" 35 minutes ago Exited (0) 35 minutes ago cranky_shannon
ff848049bc55 redmine "/docker-entrypoint.…" About an hour ago Exited (0) About an hour ago inspiring_babbage
fe67ab61abda redmine "/docker-entrypoint.…" About an hour ago Exited (0) About an hour ago cocky_bartik
65a554844970 bitnami/redmine "/app-entrypoint.sh …" About an hour ago Exited (1) About an hour ago upbeat_pare
```

 

docker rm container

```
$ docker rm 4c5784e79dd9
```
