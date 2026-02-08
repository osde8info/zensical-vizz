---
title: "podman - rootlessport cannot expose privileged port"
date: 2022-12-23
categories: 
  - "vizz"
---

if podman is giving you a rootlessport cannot expose privileged port error you need to chose a port number ABOVE 1024

```
Error message: 
Internal Server Error: 
rootlessport cannot expose privileged port 80, 
you can add 'net.ipv4.ip_unprivileged_port_start=80' to /etc/sysctl.conf (currently 1024), 
or choose a larger port number (>= 1024): 
listen tcp 0.0.0.0:80: bind: permission denied
```
