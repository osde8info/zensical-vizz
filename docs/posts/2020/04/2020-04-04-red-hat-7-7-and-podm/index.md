---
title: "red hat 7.7+ and podman rootless containers"
date: 2020-04-04
categories: 
  - "vizz"
tags: 
  - "containers"
  - "docker"
  - "podman"
---

red hat 7.7+ and podman rootless containers

- https://access.redhat.com/documentation/en-us/red\_hat\_enterprise\_linux\_atomic\_host/7/html-single/managing\_containers/index#set\_up\_for\_rootless\_containers
- https://github.com/containers/libpod/blob/master/rootless.md

config

```
# echo "user.max_user_namespaces=10000" > /etc/sysctl.d/userns.conf
# sysctl -p /etc/sysctl.d/userns.conf
```

run

```
$ podman run alpine cat /etc/os-release

$ podman run photon ps
$ podman run -i -t photon /bin/bash

$ podman run ubuntu ps
$ podman run -i -t ubuntu /bin/bash
```

images and containers are stored in $USER/.local instead of `/var/lib/containers`

the containers have no root privileges to the operating system on the host

```
/home/$USER/.local/share/containers
/home/$USER/.local/share/containers/storage

$ ls -l /home/$USER/.local/share/containers/storage/
total 20
drwx------.  2 ddarra ddarra   27 Apr  4 23:03 libpod
drwx------.  2 ddarra ddarra    6 Apr  4 23:03 mounts
drwx------. 17 ddarra ddarra 4096 Apr  4 23:18 overlay
drwx------.  9 ddarra ddarra 4096 Apr  4 23:18 overlay-containers
drwx------.  6 ddarra ddarra 4096 Apr  4 23:18 overlay-images
drwx------.  2 ddarra ddarra 4096 Apr  4 23:18 overlay-layers
-rw-------.  1 ddarra ddarra   64 Apr  4 23:19 storage.lock
drwx------.  2 ddarra ddarra    6 Apr  4 23:03 tmp

```
