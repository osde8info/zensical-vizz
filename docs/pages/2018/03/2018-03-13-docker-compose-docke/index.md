---
title: "docker compose docker-compose.yaml"
date: 2018-03-13
categories: 
  - "vizz"
---

docker compose runs all the containers (and dependancies) defined in your docker-compose.yaml file

for example

```
$ docker-compose up -d nginx
```

actually runs the nginx, phpfpm and wordspaces because the docker-compose.yaml contains depends on

```
### NGINX Server Container ##################################

nginx:
 build:
 context: ./nginx
 args:
 - PHP_UPSTREAM_CONTAINER=${NGINX_PHP_UPSTREAM_CONTAINER}
 - PHP_UPSTREAM_PORT=${NGINX_PHP_UPSTREAM_PORT}
 volumes_from:
 - applications
 volumes:
 - ${NGINX_HOST_LOG_PATH}:/var/log/nginx
 - ${NGINX_SITES_PATH}:/etc/nginx/sites-available
 ports:
 - "${NGINX_HOST_HTTP_PORT}:80"
 - "${NGINX_HOST_HTTPS_PORT}:443"
 depends_on:
 - php-fpm
 networks:
 - frontend
 - backend

### PHP-FPM Container #######################################

php-fpm:
 build:
 context: ./php-fpm
 args:
 - INSTALL_XDEBUG=${PHP_FPM_INSTALL_XDEBUG}

expose:
 - "9000"
 depends_on:
 - workspace
 extra_hosts:
 - "dockerhost:${DOCKER_HOST_IP}"
 environment:
 - PHP_IDE_CONFIG=${PHP_IDE_CONFIG}
 networks:
 - backend

### Workspace Utilities Container ###########################

workspace:
 build:
 context: ./workspace
 args:
 - INSTALL_XDEBUG=${WORKSPACE_INSTALL_XDEBUG}
 - INSTALL_BLACKFIRE=${INSTALL_BLACKFIRE}
 - INSTALL_SOAP=${WORKSPACE_INSTALL_SOAP}
 - INSTALL_LDAP=${WORKSPACE_INSTALL_LDAP}
 - INSTALL_IMAP=${WORKSPACE_INSTALL_IMAP}
```
