---
title: "kind - kubenetes in docker #cloud #cloudops #devops"
date: 2019-08-07
categories: 
  - "vizz"
tags: 
  - "devops"
  - "docker"
  - "kind"
  - "kubenetes"
---

kind - kubenetes in docker #cloud #cloudops #devops

install docker.io

```
# aptitude install docker.io
# snap install kubectl --classic
```

then

- https://itnext.io/starting-local-kubernetes-using-kind-and-docker-c6089acfc1c0
- https://kind.sigs.k8s.io/
- https://kind.sigs.k8s.io/docs/user/quick-start/

github

- https://github.com/kubernetes-sigs/kind
- https://github.com/bsycorp/kind

kind user commands

```
$ go get -u sigs.k8s.io/kind
$ export PATH=$PATH:$(go env GOPATH)/bin
$ kind create cluster
$ kind get clusters
$ export KUBECONFIG="$(kind get kubeconfig-path --name="kind")"
$ kubectl cluster-info

```
