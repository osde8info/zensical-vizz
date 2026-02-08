---
title: "howto #ssh into an @oracle cloud #oci instance without a opc password or ssh key #sysadmin"
date: 2022-01-12
categories: 
  - "vizz"
---

howto #ssh into an @oracle cloud #oci instance without a opc password or ssh key

- https://docs.oracle.com/en-us/iaas/Content/Compute/Tasks/accessinginstance.htm

or goto

- https://cloud.oracle.com/compute/instances

click

- resources
- console connection
- create local connection
- upload public ssh
- generate ssh command

cut & paste generated ssh command into your local sh

```
$ ssh -o ProxyCommand='ssh -W %h:%p -p 443 ocid1.instanceconsoleconnection.oc1.uk-london-1.WXYZ@instance-console.uk-london-1.oci.oraclecloud.com' \
-N -L localhost:5900:ocid1.instance.oc1.uk-london-1.WXYZ:5900 ocid1.instance.oc1.uk-london-1.WXYZ
```

refs

- http://www.happymillfam.com/login-to-new-oci-linux-instance-via-console/
- https://docs.oracle.com/en/cloud/get-started/subscriptions-cloud/csgsg/index.html
- https://docs.oracle.com/en-us/iaas/Content/GSG/Concepts/baremetalintro.htm
