---
title: "Develop locally - Deploy globally - with the IBM Bluemix Cloud Developer CLI"
date: 2018-08-12
categories: 
  - "vizz"
tags: 
  - "bluemix"
  - "cloud"
  - "docker"
  - "ibm"
---

Develop locally - Deploy globally - with the IBM Bluemix Cloud Developer CLI

https://console.bluemix.net/docs/cli/idt/index.html#developing

_How local containers are used_

_The IBM® Cloud® Developer Tools CLI uses two containers to facilitate building and testing your application. The first is the tools container, which contains the necessary utilities to build and test your application. The Dockerfile for this container is defined by the dockerfile-tools parameter. You might think of it as a development container as it contains the tools normally used for development of a particular runtime._

_The second container is the run container. This container is of a form suitable to be deployed for use, for example, in IBM® Cloud. As a result, an entry point is defined that starts your application. When you select to run your application through the Developer Tools CLI, it uses this container. The Dockerfile for this container is defined by the dockerfile-run parameter._
