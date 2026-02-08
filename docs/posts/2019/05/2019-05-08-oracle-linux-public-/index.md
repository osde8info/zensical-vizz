---
title: "oracle linux public yum repo info has been modularised"
date: 2019-05-08
categories: 
  - "vizz"
tags: 
  - "oracle"
  - "yum"
---

since jan 2019 oracle linux public yum repo info has been modularised

https://docs.oracle.com/cd/E52668\_01/F14052/html/notice\_description.html

_You should update your systems to use the modular yum configuration as soon as possible._

new oracle linux yum docs

- https://docs.oracle.com/cd/E52668\_01/F14052/html/checking.html
- https://docs.oracle.com/cd/E52668\_01/F14052/html/recovery.html

and if installing on virtualbox from the oracle linux 7 ISO you should enable networking in your vm and use the following oracle linux public yum network location

- http://yum.oracle.com/repo/OracleLinux/OL7/latest/x86\_64

when virtualbox guest additions says it needs kernel headers what it really means is that it needs kernel- devel

```
# yum install kernel-devel
```
