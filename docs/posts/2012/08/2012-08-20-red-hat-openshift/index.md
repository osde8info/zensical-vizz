---
title: "red hat openshift"
date: 2012-08-20
categories: 
  - "vizz"
tags: 
  - "openshift"
  - "red-hat"
---

you dont need rhc to modify your red hat openshift app just git

- [access.redhat.com/knowledge/docs/OpenShift/2.0/html/User\_Guide/clone](https://access.redhat.com/knowledge/docs/en-US/OpenShift/2.0/html/User_Guide/sect-User_Guide-Creating_Applications-Cloning_Application_Files.html)
- [access.redhat.com/knowledge/docs/OpenShift/2.0/html/User\_Guide/add](https://access.redhat.com/knowledge/docs/en-US/OpenShift/2.0/html/User_Guide/sect-User_Guide-OpenShift_Web_Interface-Editing_and_Deploying_Applications.html)
- [access.redhat.com/knowledge/docs/OpenShift/2.0/html/User\_Guide/commit](https://access.redhat.com/knowledge/docs/en-US/OpenShift/2.0/html/User_Guide/sect-User_Guide-OpenShift_Web_Interface-Editing_and_Deploying_Applications.html)
- [access.redhat.com/knowledge/docs/OpenShift/2.0/html/User\_Guide/push](https://access.redhat.com/knowledge/docs/en-US/OpenShift/2.0/html/User_Guide/sect-User_Guide-Editing_and_Deploying_Applications-Deploying_Your_Application_to_the_Cloud.html)

just

- git clone ssh://RHOSUSER@RHOSAPPNAME-RHOSDOMAIN.rhcloud.com/~/git/RHOSAPPNAME.git/
- cd RHOSAPPNAME
- cd php
- vi index.php
- git add .
- git commit -m 'my changes'
- git push
