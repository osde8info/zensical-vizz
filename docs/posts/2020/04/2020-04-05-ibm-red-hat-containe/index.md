---
title: "ibm red hat container registry requires login"
date: 2020-04-05
categories: 
  - "vizz"
tags: 
  - "container"
  - "ibm-red-hat"
  - "registry"
---

before you can podman pull from the ibm red hat container registry you need to podman login to your ibm red hat service account / subscription

```
$ podman login registry.connect.redhat.com
Username: ${REGISTRY-SERVICE-ACCOUNT-USERNAME}
Password: ${REGISTRY-SERVICE-ACCOUNT-PASSWORD}
Login Succeeded!

$ podman pull registry.connect.redhat.com/zabbix/zabbix-web-mysql-44
```

ibm red hat 7 atomic image

- https://access.redhat.com/containers/#/registry.access.redhat.com/rhel7-atomic
