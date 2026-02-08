---
title: "openshift environment variables"
date: 2012-08-22
categories: 
  - "vizz"
tags: 
  - "environment-variables"
  - "mysql"
  - "openshift"
---

you can find out your openshift mysql host, openshift mysql user and openshift mysql password by looking at your openshift environment variables

- $ ssh myopenshiftuser@myopenshiftdomain
- $ env | grep OPENSHIFT

more information on environment variables

_OpenShift provides several environment variables to reference for ease of use._

_The following list are some common variables but far from exhaustive:_

_$\_ENV\['OPENSHIFT\_APP\_NAME'\] - Application name_ _$\_ENV\['OPENSHIFT\_GEAR\_DIR'\] - Application dir_ _$\_ENV\['OPENSHIFT\_DATA\_DIR'\] - For persistent storage (between pushes)_ _$\_ENV\['OPENSHIFT\_TMP\_DIR'\] - Temp storage (unmodified files deleted after 10 days)_

_When embedding a database using 'rhc app cartridge add', you can reference environment variables for username, host and password:_

_$\_ENV\['OPENSHIFT\_DB\_HOST'\] - DB host_ _$\_ENV\['OPENSHIFT\_DB\_PORT'\] - DB Port_ _$\_ENV\['OPENSHIFT\_DB\_USERNAME'\] - DB Username_ _$\_ENV\['OPENSHIFT\_DB\_PASSWORD'\] - DB Password_

and you can use these in your drupal, wikkawiki, wordpress config file as follows

`/** The name of the database for your lamp app */ define('DB_NAME', $_ENV['OPENSHIFT_APP_NAME']); /** MySQL database username */ define('DB_USER', $_ENV['OPENSHIFT_DB_USERNAME']); /** MySQL database password */ define('DB_PASSWORD', $_ENV['OPENSHIFT_DB_PASSWORD']); /** MySQL hostname */ define('DB_HOST', $_ENV['OPENSHIFT_DB_HOST']);`
