---
title: "docker-compose exec --user"
date: 2018-03-13
categories: 
  - "vizz"
tags: 
  - "docker"
  - "exec"
  - "user"
---

if you are using docker-compose exec dont forget to use the --user switch

```shell
docker-compose exec --user=laradock workspace bash
```

see

- http://laradock.io/getting-started/
