---
title: "virtualbox @zabbix appliance #sysadmin #netadmin"
date: 2019-01-16
categories: 
  - "vizz"
tags: 
  - "netadmin"
  - "sysadmin"
  - "zabbix"
---

virtualbox @zabbix 4.0 LTS appliance #sysadmin #netadmin

- download vmdk from https://www.zabbix.com/download\_appliance
- read manual https://www.zabbix.com/documentation/4.0/manual/appliance
- create a vm without a disk and with a  bridged network
- copy vmdk into vm subdir
- add disk to vm
- login as U:appliance P:zabbix
- sudo -i
- dhcpclient
- ifconfig
- leave vm
- goto ip addr in a browser
- login as U:Admin P:zabbix

![zab](https://vizz8info.wordpress.com/wp-content/uploads/2019/01/zab.png)
