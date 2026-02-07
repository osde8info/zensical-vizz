---
title: "AMI MySQL cluster database access"
date: 2009-10-02
categories: 
  - "vizz"
tags: 
  - "cloudfoundry"
  - "cluster"
  - "ec2"
---

One of the challenges when deploying MySQL databases and clusters on Amazon EC2 AMIs is that the IP address of the AMIs are assigned dynamically. If your topology involves only a single instance then you can simply use localhost to access your MySQL server.

[Cloud Foundry](http://www.cloudfoundry.com/getting_started.html "cloudfoundry") solves this problem by ensuring that 'dbmaster' always resolves to the IP address of the MySQL server or lets you launch the application with system property that specifies the MySQL server hostname.

_Using the JVM option "-DdbHostName=${databasePrivateDnsName}" sets the the system property'dbHostName' to the MySQL server's host name. A Spring/Java application can then use a PropertyPlaceholderConfigurer bean to substitute this value into the database url, e.g. jdbc:mysql://${dbHostName}:3306/._
