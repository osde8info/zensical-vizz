---
title: "run kubernetes minikube in a vm or in a linux docker host"
date: 2019-03-13
categories: 
  - "vizz"
tags: 
  - "kubernetes"
  - "minikube"
---

run kubernetes minikube in a vm or in a linux docker host

in a vm

- https://www.linux.com/learn/getting-started-kubernetes-easy-minikube

in a linux docker host

- https://kubernetes.io/docs/tasks/tools/install-minikube/

_Minikube also supports a `--vm-driver=none` option that runs the Kubernetes components on the host and not in a VM. Using this driver requires Docker and a Linux environment but not a hypervisor._

```
# aptitude install docker.io

```

then

```
$ minikube start --vm-driver=none

😄  minikube v0.35.0 on linux (amd64)
🤹  Configuring local host environment ...

⚠️  The 'none' driver provides limited isolation and may reduce system security and reliability.
⚠️  For more information, see:
👉  https://github.com/kubernetes/minikube/blob/master/docs/vmdriver-none.md

⚠️  kubectl and minikube configuration will be stored in /root
⚠️  To use kubectl or minikube commands as your own user, you may
⚠️  need to relocate them. For example, to overwrite your own settings:

    ▪ sudo mv /root/.kube /root/.minikube $HOME
    ▪ sudo chown -R $USER $HOME/.kube $HOME/.minikube

💡  This can also be done automatically by setting the env var CHANGE_MINIKUBE_NONE_USER=true
🔥  Creating none VM (CPUs=2, Memory=2048MB, Disk=20000MB) ...
📶  "minikube" IP address is 10.0.2.15
🐳  Configuring Docker as the container runtime ...
✨  Preparing Kubernetes environment ...
💾  Downloading kubeadm v1.13.4
💾  Downloading kubelet v1.13.4
🚜  Pulling images required by Kubernetes v1.13.4 ...

```

see also

- https://docs.microsoft.com/en-us/sql/big-data-cluster/deploy-on-minikube?view=sqlallproducts-allversions
