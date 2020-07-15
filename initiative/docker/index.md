---
author: Matt
date: 2014-08-07 17:50:44+00:00
layout: page
link: http://www.researchobject.org/initiative/docker/
slug: docker
title: Docker
tags:
- Aggregation
- Containers
- Dependencies
- Description
- Exchange
- Executable
- Identity
- Linux
- Versioning
- Virtualization
---
Dockers is essentially two things











	
  1. A twenty first century version of make (using Dockerfiles),

	
  2.  a virtualisation solution (using the Docker Engine and Docker Images).










 “Dockerfiles" are used to describe how to package up or “Dockerize" almost any linux-based application, describing things like **dependencies**, what system resources are needed (e.g. ports), and how to run the application.







You can then build and pass around  Dockerized applications as Docker Images that can be executed. Anyone with the Docker engine installed can execute the image.







Docker images are executed in their own ‘container’ - a partitioned off, sandboxed execution environment - that provides two benefits:











	
  * the person who creates the image has a predictable execution environment,

	
  * the person who executes it doesn’t need to worry about it doing anything unwanted to their machine.










 Docker Images are a type of RO in that they are an **aggregation** of stuff, complete with **description** of how that stuff fits together - and it just so happens that that description is **executable**.
