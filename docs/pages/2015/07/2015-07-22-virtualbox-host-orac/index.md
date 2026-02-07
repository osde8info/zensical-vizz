---
title: "#virtualbox host oracle #linux guest howto"
date: 2015-07-22
categories: 
  - "vizz"
tags: 
  - "gnu-linux"
  - "oracle"
  - "virtualbox"
---

https://www.virtualbox.org/manual/ch02.html#externalkernelmodules

https://www.virtualbox.org/manual/ch04.html#idp96235792

after building a virtualbox oracle linux 6 vm from the dvd iso you will need to login as root and

```
# ifup eth0
# yum update
# reboot

# ifup eth0
# yum install gcc
# yum install kernel-devel
# yum install kernel-headers
```

before installing guest additions by running ./VBoxLinuxAdditions.run

```
# cd /media/VBox
# ./VBoxLinuxAddittions.run
# reboot
```
