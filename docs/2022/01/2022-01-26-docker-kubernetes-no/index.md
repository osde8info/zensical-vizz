---
title: "docker @kubernetes non-root and rootless hacks #devops #sysadmin"
date: 2022-01-26
categories: 
  - "vizz"
---

docker @kubernetes non-root and rootless hacks #devops #sysadmin

after you install docker you can

manage docker as a nonroot user (THIS IS A HACK)

- https://docs.docker.com/engine/install/linux-postinstall/

the better way (BUT MORE COMPLICATED) is to run docker as a nonroot user

- https://docs.docker.com/engine/security/rootless/

if you havent done one of the above you will get /var/run/docker.socket connect permission denied errors when running docker or minikube start or minikube stop

```
❌  Exiting due to GUEST_STOP_TIMEOUT: docker container inspect minikube --format=: exit status 1
stdout:

stderr:
Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: 
Get http://%2Fvar%2Frun%2Fdocker.sock/v1.24/containers/minikube/json: dial unix /var/run/docker.sock: connect: permission denied
```
