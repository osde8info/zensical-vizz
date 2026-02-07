---
title: "linuxlite docker super quick install"
date: 2018-03-12
categories: 
  - "vizz"
---

linuxlite docker super quick install on linuxlite running natively or in a vmware workstation player vm (it might even work in an oracle virtualbox vm)

```
# aptitude update
# aptitude install apt-transport-https ca-certificates curl software-properties-common
# curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add -
# apt-key fingerprint 0EBFCD88
# add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
 $(lsb_release -cs) \
 stable"
# aptitude update
# aptitude install docker-ce
# usermod -aG docker MYUSERNAME
```

 

logout and login to X windows then run

```
$ docker run hello-world
```

 

Refs

- https://docs.docker.com/install/linux/docker-ce/ubuntu/#install-docker-ce-1
