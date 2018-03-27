---
layout: post
title: The dummies guide to the Kubernetes Ecosystem

date: 2018-03-27
categories: containers
tags: kubernetes, containers 
excerpt_separator: <!--more-->
---

I will do a series a blog as I get my head wrapped around Kubernetes. 

A recent proclamation in the technology trends is that Kubernetes has won the container wars. It implies that 
Kubernetes is the new operating system for the cloud. 

# What is Kubernetes (k8s)?
One of the key misconceptions is that k8s is an orchestration engine for docker containers. This is how I thought about it.
That is true but it is much more.
<p></p>

Container orchestration is a key capability of the platform but there is much more. I think of k8s as the 
container orchestrator and the ecosystem services around it. Here are the key services that a company needs to think about
as they bring in k8s:

* Container scheduler, orchestration and runtime: the runtime are the services like network, filesystem that containers need to 
use to function; the scheduler schedules containers to run in a cluster; the orchestrator manages the SLA for the system. 
* API and management UI: every service in k8s is available through an API service and the management UX uses the API to provide the UX
* Registry (docker registry): The service registry is where you look up docker containers that are provisioned by the runtime
* Service discovery: all the services provided in k8s are discoverable through this service
* Security and Governance policies: secret management, rbac, image protection and the overall resource policies fall here
* Monitoring: if you have imagined a criss-cross of services, containers and messages flying around - you are right about it. 
A system like this needs a monitoring system. 

So if you are bringing k8s in-house or evaluating a cloud solution, you need to think about the above categories of service
and make sure that your provider is providing an acceptable service (for you) on each of the categories.

 

