---
title: "docker on linuxlite and ed/x/ubuntu"
date: 2018-03-11
categories: 
  - "vizz"
tags: 
  - "docker"
  - "linuxlite"
  - "xubuntu"
---

how to install docker-ce on linuxlite and ed/x/ubuntu

- https://docs.docker.com/install/linux/docker-ce/ubuntu/
- https://store.docker.com/editions/community/docker-ce-server-ubuntu
- https://store.docker.com/editions/community/docker-ce-server-ubuntu/plans/docker-ce-server-ubuntu-tier?tab=instructions

quickstart

```
# aptitude update
# aptitude install apt-transport-https \
 ca-certificates \
 curl \
 software-properties-common
```

```
# curl -fsSL https://download.docker.com/linux/ubuntu/gpg \
| apt-key add -
```

```
# apt-key fingerprint 0EBFCD88

```

```
# add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
```

```
then finally 

# aptitude update
# aptitude install docker-ce
```
