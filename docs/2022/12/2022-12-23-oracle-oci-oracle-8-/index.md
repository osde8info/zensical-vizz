---
title: "oracle oci oracle 8 how to enable cockpit access over public internet"
date: 2022-12-23
categories: 
  - "vizz"
---

oracle oci oracle linux 8 how to enable cockpit access over public internet

FIRST create an INGRESS rule for 0.0.0.0/0 to 9090/TCP

```
No	0.0.0.0/0	TCP	All	80		TCP traffic for : 80
```

SECOND open oracle linux 8 firewalld

```
# firewall-cmd --permanent --zone=public --add-port=9090/tcp
# firewall-cmd --reload
# firewall-cmd --zone=public --list-ports
9090/tcp
```

or SECOND open ubuntu 22 iptables

```
# iptables -I INPUT 6 -m state --state NEW -p tcp --dport 9090 -j ACCEPT
# netfilter-persistent save

# iptables -L
ACCEPT     tcp  -- anywhere             anywhere             state NEW tcp dpt:9090
```

see also

https://cockpit-project.org/guide/latest/listen.html#listen-firewalld

[![](https://vizz8info.wordpress.com/wp-content/uploads/2022/12/image-5.png?w=1024)](https://vizz8info.wordpress.com/wp-content/uploads/2022/12/image-5.png)
