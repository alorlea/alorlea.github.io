---
layout: post
title: Developing Applications With Docker
modified:
categories: posts
description:
tags: [docker, intellij, distributed applications]
image:
  feature:
  credit:
  creditlink:
comments: true
share: true
date: 2015-08-13T14:05:10+02:00
---

Recently, I had the opportunity to get my hands dirty playing with docker containers in my workplace with the purpose of
containerazing our applications and increase our velocity when deploying running software into our hardware. I have been
focusing on how to simplify handling a distributed applications deployment where different services 
(Frontend services, Backend Services and Data services) need to interact in isolated and repeatable environments. 

So far the experience has been quite promising on how easy it is to create a container, if we compare it to building for 
example a simple AMI (Amazon Image) in Amazon Web Services where it involves running Amazon EC2 tools in the Virtual 
Machine we want to create the image from.

In this post, I will go over the process of working with docker in your local machine.

## What is Docker?

Docker is a virtualization technology that focuses on the simple premise of allowing developers and devops to package their
applications and dependencies in a medium which allows easier portability among different machines & environments while 
maintaining a high level of flexibility.

We can tend to think, that docker containers are like normal virtual machines, yet in reality they are more light weight
compared to normal vms, as it fine tunes the resources available in the virtualized instance by removing guest OS dependencies
and the need of using of a hypervisor, which in involves in an extra overhead to deal with.

So containers deployed in the same machine, tend to share external resources provided by the host OS where docker is 
running like the kernels OS, filesystem and disk usage.