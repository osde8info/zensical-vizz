---
title: "howto install @microsoft #azdata cli on @redhat, @fedora, @centos &amp; @oracle gnu/linux 7 &amp; 8 #azure #cloud #dba #devops #sysadmin"
date: 2020-11-27
categories: 
  - "vizz"
---

howto install @microsoft #azdata on @redhat, @fedora, @centos & @oracle gnu/linux 7 & 8

```
# rpm --import https://packages.microsoft.com/keys/microsoft.asc

7

# yum-config-manager --add-repo https://packages.microsoft.com/yumrepos/mssql-server-2019-rhel7/
# yum install azdata-cli 

8

# dnf config-manager --add-repo https://packages.microsoft.com/yumrepos/mssql-server-2019-rhel8/
#dnf install azdata-cli
```
