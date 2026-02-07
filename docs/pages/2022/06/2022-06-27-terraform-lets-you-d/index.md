---
title: "Terraform lets you define resources and infrastructure in configuration files, and manages your infrastructure's lifecycle."
date: 2022-06-27
categories: 
  - "vizz"
---

Terraform is HashiCorp's infrastructure as code tool. It lets you define resources and infrastructure in human-readable, declarative configuration files, and manages your infrastructure's lifecycle. 

- https://learn.hashicorp.com/tutorials/terraform/infrastructure-as-code?in=terraform/docker-get-started

install

```
# aptitude install curl
# curl -fsSL https://apt.releases.hashicorp.com/gpg | tee /etc/apt/trusted.gpg.d/hashi.asc
# apt-add-repository "deb [arch=amd64] https://apt.releases.hashicorp.com $(lsb_release -cs) main"
# aptitude install terraform
```

run

```
$ terraform
```

create main.tf

```
terraform {
  required_providers {
    docker = {
      source  = "kreuzwerker/docker"
      version = "~> 2.13.0"
    }
  }
}

provider "docker" {}

resource "docker_image" "nginx" {
  name         = "nginx:latest"
  keep_locally = false
}

resource "docker_container" "nginx" {
  image = docker_image.nginx.latest
  name  = "tutorial"
  ports {
    internal = 80
    external = 8000
  }
}
```

then

```
$ terraform init
$ terraform apply
```
