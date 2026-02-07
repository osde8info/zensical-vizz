---
title: "how to install @virtualbox #guest tools on @mx_linux gnu/linux #distro"
date: 2019-09-01
categories: 
  - "vizz"
tags: 
  - "mx_linux"
  - "virtualbox"
---

to install @virtualbox #guest tools on @mx\_linux gnu/linux #distro first remove the broken pre-installed virtualbox packages

```
# aptitude remove virtualbox-guest-x11
# aptitude remove virtualbox-guest-utils
# aptitude remove virtualbox-dkms
# aptitude remove virtualbox-guest-dkms
```

then reboot and mount virtualbox guest additions cd and run VBoxLinuxInstall
