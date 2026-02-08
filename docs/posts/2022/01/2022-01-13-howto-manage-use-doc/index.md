---
title: "howto manage/use @docker from a non root user and howto run @docker as a non root user #cloud #sysadmin"
date: 2022-01-13
categories: 
  - "vizz"
---

howto manage/use @docker from a non root user and howto run @docker as a non root user #cloud #sysadmin

howto run docker rootless

- https://docs.docker.com/engine/security/rootless/
- https://docs.docker.com/engine/security/rootless/#:~:text=%20Run%20the%20Docker%20daemon%20as%20a%20non-root,have%20added%20them%20to%20~%2F.bashrc.%20To…%20More%20

howto manage/use docker as non-root

- https://docs.docker.com/engine/install/linux-postinstall/

these steps should stop you getting the error

```
$ docker run hello-world
docker: Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Post http://%2Fvar%2Frun%2Fdocker.sock/v1.24/containers/create: dial unix /var/run/docker.sock: connect: permission denied.

See 'docker run --help'.
```
