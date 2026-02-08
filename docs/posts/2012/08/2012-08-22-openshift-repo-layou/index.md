---
title: "openshift repo layout"
date: 2012-08-22
categories: 
  - "vizz"
tags: 
  - "openshift"
  - "php"
  - "repo"
---

your actual php code can be found in ~/app-root/runtime/repo/php

more openshift repo layout info

_Repo layout_ _\===========_ _php/ - Externally exposed php code goes here_ _libs/ - Additional libraries_ _misc/ - For not-externally exposed php code_ _../data - For persistent data (full path in environment var: OPENSHIFT\_DATA\_DIR)_ _deplist.txt - list of pears to install_ _.openshift/action\_hooks/pre\_build - Script that gets run every git push before the build_ _.openshift/action\_hooks/build - Script that gets run every git push as part of the build process (on the CI system if available)_ _.openshift/action\_hooks/deploy - Script that gets run every git push after build but before the app is restarted_ _.openshift/action\_hooks/post\_deploy - Script that gets run every git push after the app is restarted_ _Notes about layout_ _\==================_ _Please leave php, libs and data directories but feel free to create additional directories if needed._ _Note: Every time you push, everything in your remote repo dir gets recreated please store long term items (like an sqlite database) in ../data which will persist between pushes of your repo._
