---
title: "creating a scalable openshift app"
date: 2012-08-18
categories: 
  - "vizz"
tags: 
  - "ha-proxy"
  - "lamp"
  - "openshift"
  - "scalable"
---

creating a scalable openshift app (you seem to have to use cli instead of gui)

- install red hat cli tools
- run cli
- $ rhc app create -a lamp -t php-5.3 -s -d
- run gui
- add mysql cartridge

you should now have an openshift lamp app with a HA proxy, php & mysql all on separate openshift gears
