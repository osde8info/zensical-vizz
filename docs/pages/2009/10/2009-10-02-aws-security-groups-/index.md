---
title: "AWS security group(s) (cloudwall(s))"
date: 2009-10-02
categories: 
  - "vizz"
tags: 
  - "amazon-ec2"
  - "ec2"
---

The default Amazon Web Services (AWS) default (security) group (aka cloudwall/firewall) only allows access to AMIs from the same group. However you and your desktop or notebook or any customers PCs will not be in this group and therefore blocked even if you have setup key pairs ([http://code.google.com/p/cloudtools/wiki/Ec2KeyPair](http://code.google.com/p/cloudtools/wiki/Ec2KeyPair "cloudtools")) !

You'll need to add security rules to ALLOW ports such as SSH (22), SMTP (25), HTTP (80) etc to be accessible from outside the group ie any IP in the world (0.0.0.0/0) instead of just that group !

Just login to your AWS Console select the Security Groups tab, select deafult group and create the new rule(s) and/or create new security groups. ([http://code.google.com/p/cloudtools/wiki/EnablingSshAccess](http://code.google.com/p/cloudtools/wiki/EnablingSshAccess "cloudtools"))

You may also want to allow your webserver instances to talk to your database servers in which case make sure you

- either ensure web servers and db servers are running in the same default group

or

- create a db servers (security) group that allow access from a web servers (security) group and make sure your webserver AMI(s) & db AMI(s) are running in the correct security group.
