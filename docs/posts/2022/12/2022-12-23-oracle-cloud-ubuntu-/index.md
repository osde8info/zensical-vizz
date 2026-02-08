---
title: "oracle cloud + ubuntu vm + cockpit + podman"
date: 2022-12-23
categories: 
  - "vizz"
---

to use oracle cloud + oracle vm or ubuntu vm with cockpit (+ podman) you will need to create a user with a password

```
# adduser NEWUSER
# passwd NEWUSER
```

you can optionally add them to the sudo group !

```
# usermod -aG sudo NEWUSER
# groupmems -g sudo -l
```

[![](https://vizz8info.wordpress.com/wp-content/uploads/2022/12/image-6.png?w=1024)](https://vizz8info.wordpress.com/wp-content/uploads/2022/12/image-6.png)
