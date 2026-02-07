---
title: "how to run @balena_io #kvm #qemu images"
date: 2020-04-14
categories: 
  - "vizz"
tags: 
  - "balena-io"
  - "cloud"
  - "iot"
  - "kvm"
  - "qemu"
---

how to run @balena\_io #kvm #qemu images

On systems with KVM support:

```
$ qemu-system-x86_64 -drive file=resin-image-qemux86-64.img, \
media=disk, cache=none, format=raw \
-net nic,model=virtio -net user \
-m 512 -nographic -machine type=pc, -smp 4 \
accel=kvm -cpu host

```

On systems without KVM support:

```
$ qemu-system-x86_64 -drive file=resin-image-qemux86-64.img, \ 
media=disk, cache=none, format=raw \
-net nic,model=virtio -net user \
-m 512 -nographic -machine type=pc -smp 4

```

see

- https://dashboard.balena-cloud.com/apps
