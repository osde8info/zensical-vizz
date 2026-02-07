---
title: "linuxlite docker process list"
date: 2018-03-12
categories: 
  - "vizz"
tags: 
  - "containers"
  - "docker"
  - "processes"
  - "sysadmin"
---

linuxlite docker containers each appear as a separate child process when you run pstree

```
 ├─cupsd
 ├─dbus-daemon
 ├─dockerd─┬─docker-containe─┬─docker-containe─┬─redis-server───3*[{redis-server}]
 │ │ │ └─6*[{docker-containe}]
 │ │ ├─docker-containe─┬─beanstalkd
 │ │ │ └─6*[{docker-containe}]
 │ │ ├─docker-containe─┬─my_init───runsvdir─┬─runsv───syslog-ng
 │ │ │ │ ├─runsv───tail
 │ │ │ │ ├─runsv
 │ │ │ │ └─runsv───cron
 │ │ │ └─6*[{docker-containe}]
 │ │ ├─docker-containe─┬─mysqld───26*[{mysqld}]
 │ │ │ └─6*[{docker-containe}]
 │ │ ├─docker-containe─┬─php-fpm───2*[php-fpm]
 │ │ │ └─6*[{docker-containe}]
 │ │ ├─docker-containe─┬─nginx───4*[nginx]
 │ │ │ └─6*[{docker-containe}]
 │ │ ├─docker-containe─┬─python
 │ │ │ └─6*[{docker-containe}]
 │ │ └─13*[{docker-containe}]
 │ ├─6*[docker-proxy───4*[{docker-proxy}]]
 │ ├─docker-proxy───3*[{docker-proxy}]
 │ └─15*[{dockerd}]
 ├─gnome-keyring-d─┬─{gdbus}
 │ ├─{gmain}
 │ └─{timer}
```
