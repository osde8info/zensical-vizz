---
title: "ubuntu / xubuntu podman install"
date: 2020-04-05
categories: 
  - "vizz"
tags: 
  - "containers"
  - "podman"
  - "ubuntu"
---

ubuntu / xubuntu podman install

```
# aptitude install curl
# $(. /etc/os-release) \
echo "deb https://download.opensuse.org/repositories/devel:/kubic:/libcontainers:/testing/xUbuntu_"${VERSION_ID}"/ /" \
> /etc/apt/sources.list.d/devel:kubic:libcontainers:testing.list
# curl -L https://download.opensuse.org/repositories/devel:/kubic:/libcontainers:/testing/xUbuntu_${VERSION_ID}/Release.key | sudo apt-key add -
# aptitude install podman
```

one nice feature of the ubuntu / xubuntu podman installer is that it sets up /etc/subuid and /etc/subgid for existing users automatically

run

```
$ podman pull clearlinux
$ podman images
$ podman run -i -t clearlinux /bin/bash
$ podman ps -a
CONTAINER ID IMAGE COMMAND CREATED STATUS PORTS NAMES
37aff5184940 docker.io/library/clearlinux:latest /bin/bash 8 minutes ago Exited (0) 4 minutes ago romantic_perlman

```

see

- https://podman.io/getting-started/installation.html
