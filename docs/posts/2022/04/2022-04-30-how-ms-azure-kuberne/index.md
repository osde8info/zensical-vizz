---
title: "How MS #Azure @Kubernetes Service and @datadog work together"
date: 2022-04-30
categories: 
  - "vizz"
---

How MS #Azure @Kubernetes Service and @datadog work together

- https://docs.microsoft.com/en-us/azure/aks/intro-kubernetes
- https://www.datadoghq.com/

_A popular solution is to use a container orchestrator like Kubernetes._

  
_According to a report that analyzed real-world usage data from 1.5 billion  
containers, almost 90 percent of containers are orchestrated. An orchestrator  
manages container workloads by scheduling, restarting, and load balancing them  
across your infrastructure based on the desired state of your cluster. This not only  
helps improve the performance and availability of your applications, but can also  
be instrumental for efficiently scheduling more containers onto fewer hosts, which  
can translate into cost savings for companies. Cloud provider–managed container  
services enable teams to modernize their applications and adopt container  
orchestration technologies like Kubernetes_

_Azure Kubernetes Service (AKS) is a hosted service for running Kubernetes, an  
open source container orchestration platform that was originally developed at  
Google. Kubernetes automates many aspects of deploying, managing, and scaling  
containerized workloads. In addition to distributing workloads across nodes in the  
cluster, Kubernetes can also automatically scale workloads based on real-time  
demand. It also helps improve the availability of mission-critical applications by  
automatically relaunching unhealthy containers and nodes as needed._

Kubernetes manifests are configuration files that define the desired state of  
objects in the cluster. Manifests describe the number of pods to provision and  
the types of containers that will run in each pod. You may also specify resource  
requirements for your workloads. Based on the information in your manifests,  
the control plane launches and schedules pods to move the cluster closer to the  
desired state of your workloads. Kubernetes uses controllers to manage the state  
of workloads in your cluster
