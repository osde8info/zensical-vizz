---
title: "docker node.js images not to be confused with the docker node command"
date: 2019-06-03
categories: 
  - "vizz"
tags: 
  - "docker"
  - "node"
  - "nodejs"
---

docker node.js images not to be confused with the docker node command

- https://github.com/nodejs/docker-node
- https://hub.docker.com/\_/node/
- https://github.com/nodejs/docker-node/blob/master/README.md#how-to-use-this-image

_how to run a single Node.js script_

_For many simple, single file projects, you may find it inconvenient to write a complete `Dockerfile`. In such cases, you can run a Node.js script by using the Node.js Docker image directly_:

```
$ docker run -it --rm --name my-running-script -v 
"$PWD":/usr/src/app -w /usr/src/app node:8 
node your-daemon-or-script.js
```

docker node command

- https://docs.docker.com/engine/reference/commandline/node/
