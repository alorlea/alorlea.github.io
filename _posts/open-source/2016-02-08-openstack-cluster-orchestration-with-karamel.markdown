---
layout: post
title: Openstack Cluster Orchestration With Karamel
modified:
categories: open-source
description:
tags: [Karamel, Openstack, orchestration]
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
in addition to baremetal setups. It is quite easy to get started, you simply need to define your cluster in a file, 
submit it to the application and do one click!

With this tool you can easily have up and a running large big data clusters with hadoop with flink or even apache spark. 
In addition, it is the preferred tool for testing out a new hadoop distribution named [HOPS](http://www.hops.io/) which address a lot of the big
inconveniences big hadoop deployments encounter (for example, how to achieve [high availability of the namenode](http://www.hops.io/?q=content/hdfs) among other enhancements

