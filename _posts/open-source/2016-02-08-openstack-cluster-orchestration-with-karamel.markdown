---
layout: post
title: Openstack Hadoop Cluster Orchestration With Karamel
modified:
categories: open-source
description:
tags: [Karamel, Openstack, Hadoop, Chef, Automation]
image:
  feature:
  credit:
  creditlink:
comments:
share:
published: false
date: 2016-02-08T17:26:30+01:00
---

This is a special post as it remarks my first contribution to a small open-source project and also to my ex-colleagues 
during my brief time at [SICS](https://www.sics.se/). This project follows up and takes further the initial 
prototype my Master Thesis was centered on orchestrating Hadoop in Platform as a Service solutions.
 
This idea has evolved and been refined into a more mature project called [Karamel](http://www.karamel.io/). Karamel is 
a very fine tool that simplifies big data deployments on a selection of cloud providers like AWS and Google Cloud Engine, 
in addition to baremetal cluster setups. It is quite easy to get started, you simply need to define your cluster in a 
file, submit it to the application and do one click!

With this tool you can easily have up a functional big data clusters with hadoop with flink or even apache spark. 
In addition, it is the preferred tool for testing out a new hadoop distribution named [HOPS](http://www.hops.io/) 
which address the inconveniences that big hadoop deployments encounter (for example, how to achieve [high 
availability of the namenode](http://www.hops.io/?q=content/hdfs))

# Introduction

In this post, I will explain how you can deploy 

In order to deploy our Hadoop cluster on Openstack, first we will need to get a copy of the latest version of 
karamel, you can do it [here](http://www.karamel.io/?q=content/getting-started-karamel). Here you will find 
guidelines to get started with other providers like AWS.

