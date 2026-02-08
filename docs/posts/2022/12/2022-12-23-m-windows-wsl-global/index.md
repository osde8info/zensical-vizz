---
title: "m$ windows wsl global settings"
date: 2022-12-23
categories: 
  - "vizz"
---

m$ windows wsl global settings

on your windows host you can create a ~/.wslconfig that will apply to ALL wsl instances

for example if you want to limit each vm to one cpu and 2GB memory

`C:\> type ~/.wslconfig`

```
[wsl2]
processors=1
memory=2GB
swap=2GB
```

of course EACH wsl vm can have its individual settings in /etc/wsl.conf

`$ cat /etc/wsl.conf`

```

[boot]
systemd=true
```

see

https://learn.microsoft.com/en-us/windows/wsl/wsl-config
