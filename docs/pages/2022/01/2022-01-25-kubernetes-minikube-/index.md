---
title: "kubernetes #minikube now supports @NVIDIA #GPU"
date: 2022-01-25
categories: 
  - "vizz"
---

kubernetes #minikube quickstart

- https://minikube.sigs.k8s.io/docs/

NOTE : typos in official docs omit DPKG -I command

root

```
# aptitude install docker
# curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube_latest_amd64.deb
# dpkg -i minikube_latest_amd64.deb
```

you

```
$ sudo usermod -aG docker $USER
$ newgrp docker
$ minikube start
```

```
you should see
```

```
$ minikube start
😄  minikube v1.25.1 on Ubuntu 20.04 (vbox/amd64)
✨  Automatically selected the docker driver
👍  Starting control plane node minikube in cluster minikube
🚜  Pulling base image ...
💾  Downloading Kubernetes v1.23.1 preload ...
```

now supports @NVIDIA #GPU

- https://minikube.sigs.k8s.io/docs/tutorials/nvidia\_gpu/

github

- https://github.com/kubernetes/minikube

<figure>

[![](https://vizz8info.wordpress.com/wp-content/uploads/2022/01/screenshot-127.0.0.1_36063-2022.01.25-23_44_29.png?w=1024)](https://vizz8info.wordpress.com/wp-content/uploads/2022/01/screenshot-127.0.0.1_36063-2022.01.25-23_44_29.png)

<figcaption>

kube dash

</figcaption>

</figure>

[![](https://vizz8info.wordpress.com/wp-content/uploads/2022/01/screenshot-127.0.0.1_39707-2022.01.25-23_51_42.png?w=1024)](https://vizz8info.wordpress.com/wp-content/uploads/2022/01/screenshot-127.0.0.1_39707-2022.01.25-23_51_42.png)
