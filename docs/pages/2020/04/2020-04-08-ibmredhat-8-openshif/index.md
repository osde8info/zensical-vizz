---
title: "ibmredhat 8 &amp; @OpenShift #container management #devops"
date: 2020-04-08
categories: 
  - "vizz"
tags: 
  - "buildah"
  - "containers"
  - "ibmredhat"
  - "openshift"
  - "podman"
  - "skopeo"
---

ibmredhat 8 & @OpenShift #container management #devops

ibmredhat _have removed the Docker container engine, along with the docker command, from Red Hat Enterprise Linux 8 entirely. For RHEL 8, Docker is not included and not supported by Red Hat (although it is still available from other sources)_

- Xhttps://access.redhat.com/documentation/en-us/red\_hat\_enterprise\_linux/8/pdf/building\_running\_and\_managing\_containers/Red\_Hat\_Enterprise\_Linux-8-Building\_running\_and\_managing\_containers-en-US.pdfX

with ibmredhat the focus _is not on running individual containers from the command line. The primary venue for running containers is a Kubernetes-based platform, such as OpenShift._

_By repositioning OpenShift as the project for running containers, container engines like Docker become just another component of OpenShift with no direct access by end users._

_Because the container engine in OpenShift is not meant to be used directly, it can be_ _implemented with a limited feature set that focuses on doing everything that OpenShift needs, without having to implement lots of standalone features_

_Tools like podman, skopeo, and buildah were developed to take over those docker command features._

the newworld tools are

- [buildah](https://github.com/containers/buildah)
- [libpod / podman](https://github.com/containers/libpod/tree/master/cmd/podman)
- runc
- [skopeo](https://github.com/containers/skopeo)

ibmredhat universal base image (UBI) containers

- https://access.redhat.com/articles/4238681
- http://registry.access.redhat.com/ubi8/ubi:latest

to build a container run buildah

```
$ buildah bud -t mycontainer

Dockerfile
FROM registry.access.redhat.com/ubi8/ubi
ADD myecho /usr/local/bin
ENTRYPOINT "/usr/local/bin/myecho"
CMD "/usr/local/bin/myecho"

myecho
echo "This container works!"
```

to manage, run, stop, start a container use podman

```
$ podman run -i -t -p 8080:80 --name=pho photon /bin/bash
$ podman inspect --format='{{.Path}}' pho
$ podman logs pho
$ podman stop pho
$ podman start -i -a pho
```

to copy containers use skopeo

```
$ skopeo
```
