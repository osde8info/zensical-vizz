---
title: "Red Hat OpenShift Client Install"
date: 2012-08-17
categories: 
  - "vizz"
tags: 
  - "client"
  - "cloud"
  - "openshift"
  - "red-hat"
---

Red Hat OpenShift Client Install

Documentation

- [access.redhat.com/knowledge/docs/OpenShift/](https://access.redhat.com/knowledge/docs/OpenShift/)
- [access.redhat.com/knowledge/docs/OpenShift/Getting\_Started\_Guide](https://access.redhat.com/knowledge/docs/en-US/OpenShift/2.0/html/Getting_Started_Guide/sect-Getting_Started_Guide-OpenShift_Client_Tools-Installing_Client_Tools.html#sect-Getting_Started_Guide-Installing_on_Windows)

Windoz Apps & Utilities

- [rubyinstaller.org/](http://rubyinstaller.org/)
- [msysgit.github.com/](http://msysgit.github.com/)

OpenShift bash / shell / ssh commands

- $ gem install rhc
- $ rhc setup  - (this will automatically set up ssh key for you)
- $ rhc domain show
- $ ssh UUID@MYOPENSHIFTAPPDNSNAME

Note you can get UUID & MYOPENSHIFTAPPDNSNAME from the output of

"rhc domain show"

Add your own domain name to Red Hat OpenShift DNS

- $ rhc app add-alias -a MYAPPNAME --alias "MY.EXAMPLE.COM"
- add a CNAME for MY.EXAMPLE.COM that points to MYOPENSHIFTAPPDNSNAME
