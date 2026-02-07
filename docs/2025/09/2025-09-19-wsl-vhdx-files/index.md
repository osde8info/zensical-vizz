---
title: "wsl vhdx files"
date: 2025-09-19
categories: 
  - "vizz"
---

wsl vhdx files default to 1T and are kept in C:\\Users\\YOURUSERNAME\\AppData\\Local\\Packages\\DISTRONAME\\Localstate

ie

```
C:\Users\YOURUSERNAME\AppData\Local\Packages\DISTRONAME\LocalState\ext4.vhdx
```

import & export (& move)

```
wsl --export DISTRONAME D:\Backup\DISTRONAME.tar
wsl --unregister DISTRONAME
wsl --import DISTRONAME D:\WSL\DISTRONAME D:\Backup\DISTRONAME.tar --version 2
```

WSL Settings

[![](https://vizz8info.wordpress.com/wp-content/uploads/2025/09/image.png?w=1024)](https://vizz8info.wordpress.com/wp-content/uploads/2025/09/image.png)
