---
title: "linuxliteos docker security hardening"
date: 2018-03-11
categories: 
  - "vizz"
tags: 
  - "docker"
  - "hardening"
  - "linuxlite"
  - "security"
---

linuxliteos docker security hardening

- https://docs.docker.com/engine/security/security/#other-kernel-security-features
- https://docs.docker.com/engine/security/security/#conclusions

 

Add your user to the docker group.

```
$ sudo usermod -aG docker $USER
```

 

Log out and log back in so that your group membership is re-evaluated.

If testing on a virtual machine, it may be necessary to restart the virtual machine for changes to take effect.

**On a desktop Linux environment such as X Windows, log out of your session completely and then log back in.**

Verify that you can run docker commands without sudo.

```
$ docker run hello-world
```
