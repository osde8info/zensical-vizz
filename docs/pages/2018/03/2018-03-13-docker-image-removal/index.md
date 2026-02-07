---
title: "docker image removal"
date: 2018-03-13
categories: 
  - "vizz"
tags: 
  - "delete"
  - "docker"
  - "image"
  - "remove"
---

docker image deletion and removal

get a list of images

```
$ docker images --all
REPOSITORY TAG IMAGE ID CREATED SIZE
laradock_nginx latest 687eb3dccec0 23 hours ago 24.4MB
laradock_php-fpm latest 9011ae1a47a5 23 hours ago 414MB
laradock_redis latest a085dd214956 24 hours ago 107MB
laradock_workspace latest 2ea822e3b905 24 hours ago 725MB
osde8info/get-started part-2 05bbc25a892f 27 hours ago 148MB
node alpine 785e257485e7 4 days ago 68.4MB
bitnami/redmine latest e547bec0c9bb 7 days ago 708MB
postgres alpine f4f4231d6f0b 10 days ago 39.5MB
```

delete a specific image

```
$ docker image rm f4f4231d6f0b
```
