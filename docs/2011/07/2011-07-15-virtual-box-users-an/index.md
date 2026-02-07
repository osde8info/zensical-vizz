---
title: "virtual box users and USB access"
date: 2011-07-15
categories: 
  - "vizz"
tags: 
  - "virtual-box"
---

The virtualbox gnu/inux installers create [the system user group vboxusers](http://www.virtualbox.org/manual/ch02.html#idp5640144 "virtualbox") during installation.

Any system user who is going to use USB devices from VirtualBox guests must be member of that group.

A user can be made member of the group vboxusers through the GUI user/group management or at the command line with

```
# usermod -a -G vboxusers username
```

Note that adding an active user to that group will require that user to log out and back in again. This should be done manually after successful installation of the package.
