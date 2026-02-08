---
title: "openshift client on opensuse"
date: 2013-05-13
categories: 
  - "vizz"
tags: 
  - "client"
  - "cloud"
  - "install"
  - "openshift"
  - "opensuse"
  - "red-hat"
  - "rhc"
  - "sysadmin"
---

the procedure to install the red hat openshift client utilities on opensuse gnu/linux is slightly different to that on red hat gnu/linux

on red hat enterprise linux 6

- [https://www.openshift.com/get-started](https://www.openshift.com/get-started)

on opensuse 12.3  as root

- \# zypper install git
- \# zypper install rubygems
- \# zypper install rubygem-rhc

on opensuse 12.3 as you

- $ rhc setup
