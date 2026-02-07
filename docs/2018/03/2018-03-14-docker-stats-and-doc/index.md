---
title: "docker stats and docker top"
date: 2018-03-14
categories: 
  - "vizz"
---

to use docker stats and docker top get container ids from docker container list or docker ps

```
$ docker ps

CONTAINER ID IMAGE COMMAND CREATED STATUS PORTS NAMES
375fd90c86a8 laradock_nginx "nginx" About an hour ago Up About an hour 0.0.0.0:80->80/tcp, 0.0.0.0:443->443/tcp laradock_nginx_1
8433057223b9 laradock_php-fpm "docker-php-entrypoi…" About an hour ago Up About an hour 9000/tcp laradock_php-fpm_1
1f708b403022 laradock_workspace "/sbin/my_init" About an hour ago Up About an hour 0.0.0.0:2222->22/tcp laradock_workspace_1
```

 

docker stats

```
$ docker stats 375fd90c86a8
```

 

docker top

```
$ docker top 375fd90c86a8

```
