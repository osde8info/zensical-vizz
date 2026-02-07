---
title: "docker images are kept in /var/lib/docker"
date: 2018-03-13
categories: 
  - "vizz"
tags: 
  - "containers"
  - "docker"
  - "images"
---

docker images are kept in /var/lib/docker

```
# du -s /var/lib/docker/*
20    /var/lib/docker/builder
220   /var/lib/docker/containerd
884   /var/lib/docker/containers
30028 /var/lib/docker/image
84    /var/lib/docker/network
5876620 /var/lib/docker/overlay2
20    /var/lib/docker/plugins
4     /var/lib/docker/runtimes
4     /var/lib/docker/swarm
4     /var/lib/docker/tmp
4     /var/lib/docker/trust
188   /var/lib/docker/volumes
```

you can save a lot of space by deleting any unused images and containers

```
# du -s /var/lib/docker/*
20	/var/lib/docker/builder
220	/var/lib/docker/containerd
4	/var/lib/docker/containers
2888	/var/lib/docker/image
84	/var/lib/docker/network
163380	/var/lib/docker/overlay2
20	/var/lib/docker/plugins
4	/var/lib/docker/runtimes
4	/var/lib/docker/swarm
4	/var/lib/docker/tmp
4	/var/lib/docker/trust
188	/var/lib/docker/volumes

```
