---
title: "m$ wsl running multiple linux instances"
date: 2022-12-24
categories: 
  - "vizz"
---

m$ wsl lets you run multiple gnu/linux distros/instances but they all share the same vnet card so systemd services such as HTTPD, SSHD, COCKPIT will fail to start on secondary instances unless you change the ip and / or socket they are listening on

you can even create multiple clones of the same distro via a TAR file (see refs)

wsl vdisks can be found in

`C:\Users\YOURUSER\AppData\Local\Packages\DISTRO`

wsl vdisk for kali is in

`C:\Users\YOURUSER\AppData\Local\Packages\KaliLinux.54290C8133FEE_ey8k8hqnwqnmg\LocalState\ext4.vhdx`

and oracle linux and ubuntu linux etc in the following subdirs

`3810OracleAmericaInc.OracleLinux8.5_dm28ctvqnhe9g`

`CanonicalGroupLimited.Ubuntu20.04onWindows_79rhkp1fndgsc`

`CanonicalGroupLimited.Ubuntu22.04LTS_79rhkp1fndgsc`

because all wsl vms SHARE the same vnet card all ports are exposed on all vms

here are 3 wsl vms using same vnet card but running services on different ports

```
# nmap localhost -p 20-9999
Starting Nmap 7.80 ( https://nmap.org ) at 2022-12-24 13:55 GMT
Nmap scan report for localhost (127.0.0.1)
Host is up (0.000024s latency).
Not shown: 2978 closed ports

PORT     STATE SERVICE
22/tcp   open  ssh
631/tcp  open  ipp

2222/tcp open  EtherNetIP-1
2233/tcp open  infocrypt

4330/tcp open  dey-sapi
4331/tcp open  ktickets-rest
4332/tcp open  unknown

9090/tcp open  zeus-admin
9092/tcp open  XmlIpcRegSvc
9191/tcp open  sun-as-jpda
```

refs

- https://endjin.com/blog/2021/11/setting-up-multiple-wsl-distribution-instances

- https://sungkim11.medium.com/why-you-should-use-multiple-instances-of-same-linux-distro-on-wsl-windows-10-f6f140f8ed88

[![](https://vizz8info.wordpress.com/wp-content/uploads/2022/12/image-7.png?w=1024)](https://vizz8info.wordpress.com/wp-content/uploads/2022/12/image-7.png)
