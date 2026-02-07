---
title: "virtualbox minishift openshift origin dev env"
date: 2017-08-30
categories: 
  - "vizz"
tags: 
  - "minishift"
  - "openshift"
  - "virtualbox"
---

if you have virtualbox (or hyper-v) you can download minishift and create a local openshift origin demo or dev environment

- https://www.openshift.org/minishift/
- https://docs.openshift.org/latest/minishift/index.html
- https://docs.openshift.org/latest/minishift/getting-started/index.html
- https://github.com/minishift/minishift/releases

to avoid the Hyper-V error you will need to run minishift with the --vm-driver switch BAD WAY

```
C:\Progs\minishift-1.5.0-windows-amd64>minishift start
-- Installing default add-ons ... OK
-- Checking if Hyper-V driver is configured ... FAIL
 Hyper-V virtual switch is not set

```

GOOD WAY

```
C:\Progs\minishift-1.5.0-windows-amd64>minishift start --vm-driver virtualbox
-- Starting local OpenShift cluster using 'virtualbox' hypervisor ...
-- Minishift VM will be configured with ...
 Memory: 2 GB
 vCPUs : 2
 Disk size: 20 GB
```

once you have minishift openshift running locally you should be able to access its  webconsole at

- https://your-local-minishift-openshift-ip:8443

and you may want to download the openshift command line tools so you can use those locally too

- https://github.com/openshift/origin/releases

once you are happy minishift openshift is running locally you may like to create a project using the demo national parks container

- https://github.com/openshift-roadshow/parksmap-web-py

and the demo national parks python app

- https://github.com/openshift-roadshow/nationalparks-katacoda

you should then see something like this

https://www.flickr.com/photos/osde-info/36779379901/in/datetaken-public/
