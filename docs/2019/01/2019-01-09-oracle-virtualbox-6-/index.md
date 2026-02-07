---
title: "oracle #virtualbox 6.x and @linuxlite 4.x"
date: 2019-01-09
categories: 
  - "vizz"
tags: 
  - "linux-lite"
  - "vbox-additions"
  - "virtualbox"
---

oracle #virtualbox 6.x and @linuxlite 4.x

uninstall (preinstalled) virtualbox-\* packages

ignore SCARY warning

```
Accept this solution? [Y/n/q/?] y
The following packages will be REMOVED:
linux-image-unsigned-4.15.0-34-generic{u} 
linux-modules-4.15.0-34-generic{u} virtualbox-guest-utils 
virtualbox-guest-x11{a}

```

then mount virtualbox iso then

```
# cd /media/virtualbox
# ./VBoxLinuxAdditions.run
```

finally reboot

note there is a bug with virtualbox 6.x and linuxlite 4.x screen does not autoresize so you have to manually change display size in the guest then resize your virtualbox window

stop press

auto screen resize now works after an

```
# aptitude safe-upgrade
```
