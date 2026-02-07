---
title: "minishift openshift and dockerhub docker images"
date: 2017-09-03
categories: 
  - "vizz"
tags: 
  - "docker"
  - "dockerhub"
  - "minishift"
  - "openshift"
  - "swagger"
---

minishift openshift should be able to import dockerhub images but most of them are not minishift openshift compatible or broken :(

```
image hello-world runs as the root user which might not be permitted by your cluster administrator
```

however there is one that does seem to work and that is the openshift swagger-ui-site

- https://hub.docker.com/r/openshift/swagger-ui-site/

```
openshift/swagger-ui-site
```
