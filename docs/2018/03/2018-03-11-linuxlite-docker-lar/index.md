---
title: "linuxlite docker laradock containers"
date: 2018-03-11
categories: 
  - "vizz"
tags: 
  - "docker"
  - "laradock"
  - "linuxlite"
---

almost got linuxlite docker laradock containers working

- docker
- http://laradock.io/

 

```
$ docker-compose ps
 Name Command State Ports 
------------------------------------------------------------------------------------------------------------
laradock_applications_1 /true Exit 0 
laradock_beanstalkd_1 /usr/bin/beanstalkd Up 0.0.0.0:11300->11300/tcp 
laradock_mysql_1 docker-entrypoint.sh mysqld Up 0.0.0.0:3306->3306/tcp 
laradock_nginx_1 nginx Up 0.0.0.0:443->443/tcp, 0.0.0.0:80->80/tcp 
laradock_php-fpm_1 docker-php-entrypoint php-fpm Up 9000/tcp 
laradock_redis_1 docker-entrypoint.sh redis ... Up 0.0.0.0:6379->6379/tcp 
laradock_workspace_1 /sbin/my_init Up 0.0.0.0:2222->22/tcp
```
