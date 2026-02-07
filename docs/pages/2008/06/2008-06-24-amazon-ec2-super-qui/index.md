---
title: "Amazon EC2 Super Quick Start with JumpBox"
date: 2008-06-24
categories: 
  - "vizz"
tags: 
  - "amazon-ec2"
  - "ami"
  - "cloud"
  - "vm-guest"
---

EC2 Quick Start

- sign up
- generate cert & private key
- download amazon ec2 tools into ~/ec2
- export environment variables
- export EC2\_HOME=~/ec2
- export JAVA\_HOME=/usr/java/jre1.5.0\_15
- export EC2\_PRIVATE\_KEY=~/ec2/pk.pem
- export EC2\_CERT=~/ec2/cert.pem
- export EC2\_JVM\_ARGS="-Dhttps.proxyHost=my.proxy -Dhttps.proxyPort=8080"

Then run amazon ec2 describe images utility

$ ./bin/ec2-describe-images -a

you'll see a list of over 600 AMIs including the following jumpboxs

- IMAGE   ami-70ab4f19    jumpbox-amis/bugzilla-1.1.0.manifest.xml
- IMAGE   ami-71ab4f18    jumpbox-amis/mediawiki-1.1.0.manifest.xml
- IMAGE   ami-6aac4803    jumpbox-amis/movabletype-1.1.0.manifest.xml
- IMAGE   ami-0eb45067    jumpbox-amis/wordpress-1.1.0.manifest.xml

just choose a JumpBox AMI virtual machine software appliance and run it !

Finally check your credit card bill the following month !
