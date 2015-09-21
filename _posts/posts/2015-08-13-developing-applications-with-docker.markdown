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

## Why is it becoming so popular?

One thing that I believe, docker is doing great is to focus on isolation and keep the behaviour identical of your application
along multiple phases environments.

Once you create your docker image and deploy it in a container, it will behave the same in your testing, staging and 
production environments like virtual machines, yet allowing faster deployments. For example, if we take a full ubuntu 
VM; it size will be more than 650MBs at least with everything configured and our application embedded in it. 
Taking the docker case, its footprint will be around the same size as if we wanted to deploy the builded package itself.

In addition, it has its own version control of the docker images, allowing incremental updates of its content 
(similarly to a version control like git); which help to keep track of the versions of your applications.

## Getting started with docker

It is quite simple to get started with docker and begin creating containers, if you use Intellij Idea you can use a 
quite nice [plugin](http://blog.jetbrains.com/idea/2015/03/docker-support-in-intellij-idea-14-1/).

You can start creating docker images easily by bundling it up with a dockerfile. This file acts like a script which 
docker follows and will generate the image for your docker container.

We will see that in a following post, where I will try to go over how docker works with a working example.