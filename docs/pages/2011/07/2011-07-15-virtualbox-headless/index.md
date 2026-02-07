---
title: "virtualbox headless"
date: 2011-07-15
categories: 
  - "vizz"
tags: 
  - "virtual-box"
---

[VirtualBox](http://www.virtualbox.org/manual/ch07.html#vboxheadless "virtualbox") comes with a front-end called [VBoxHeadless](http://www.virtualbox.org/manual/ch07.html#vboxheadless "virtualbox"), which produces no visible output on the host at all, but instead only delivers VRDP data.

That allows you create server hardware whose only purpose is to host VMs which run remotely over VRDP and so you dont need to have a graphical user interface on the server at all.

[VBoxHeadless](http://www.virtualbox.org/manual/ch07.html#vboxheadless "virtualbox") has no dependencies on the X Window system on Linux and Solaris hosts.
