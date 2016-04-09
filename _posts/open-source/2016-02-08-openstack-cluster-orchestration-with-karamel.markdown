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
during my brief time at [SICS](https://www.sics.se/). This project is a follows up on my Master Thesis which was 
centered on orchestrating Hadoop in Platform as a Service solutions.
 
This idea has evolved and been refined into a more mature project called [Karamel](http://www.karamel.io/). Karamel is 
a very fine tool that simplifies big data deployments on a selection of cloud providers like AWS and Google Cloud Engine, 
in addition to baremetal cluster setups. It is quite easy to get started, you simply need to define your cluster in a 
file, submit it to the application and do one click!

With this tool you can easily have up a functional big data clusters with hadoop with flink or even apache spark. 
In addition, it is the preferred tool for testing out a new hadoop distribution named [Hops](http://www.hops.io/) 
which address the inconveniences that big hadoop deployments encounter (for example, how to achieve [high 
availability of the namenode](http://www.hops.io/?q=content/hdfs))

# Introduction

Here I will try to describe what you need in order to make a deployment using Karamel towards an Openstack 
environment. I will go over how you can write a cluster file to be deployed using this tool and how you need to 
configure the Karamel in order to communicate with your cluster.

## Before we start

In order to deploy our Hadoop cluster on Openstack, first we will need to get a copy of the latest version of 
Karamel, you can do it [here](http://www.karamel.io/?q=content/getting-started-karamel). Here you will find 
guidelines to get started with other providers like AWS. You may download one of the available versions that have 
support for Openstack (version 0.2.0 onwards should do it) or download the source code and build the application with
 maven.
 
# Working with Karamel

Getting started with Karamel is quite easy, before launching our cluster, we will need to define the configuration of a
cluster. In a cluster definition file, we can identify 4 core elements to describe you cluster: Provider, Cookbooks, 
Attributes and Groups. 

We will go the meaning of each component through an example cluster, let's imagine that I want to deploy a 
simple Hadoop cluster with Apache Flink running a namenode and 20 datanodes using an Openstack infrastructure. In 
addition, we want to deploy a wordcount job when the cluster is ready.

{% highlight yaml %}

name: flinknova
nova:
  flavor: 3
  image: "99f4625e-f425-472d-8e21-7aa9c3db1c3e"

cookbooks:
  hadoop:
    github: "hopshadoop/apache-hadoop-chef"
    branch: "master"
  flink:
    github: "hopshadoop/flink-chef"
    branch: "master"

groups:
  namenodes:
    size: 1
    recipes:
        - hadoop::nn
        - flink::jobmanager
        - flink::wordcount
  datanodes:
    size: 20
    recipes:
        - hadoop::dn
        - flink::taskmanager
        
{% endhighlight %}

In this case, we can see 3 different code blocks gathering all the information we need for Karamel to do its job. 

The first segment of the file contains the provider specific information, for Openstack; we make use of the
  keyword nova to refer we are going to make use of the Openstack Nova Controller. Then, it will follow specific 
  parameters regarding nova which are:
  
  * __Flavor:__ This corresponds to a specific hardware configuration for the VM, this is similar to Amazon's EC2 
  instance descriptors. Openstack refers to them as flavors and each one specifies a configuration (CPU, RAM) and are
   not the same for everyone, as these are configured by the needs of the organization. To simplify this, Karamel makes
    use of the flavor id attached to your VM configuration.
   
  * __Image:__ This corresponds to the VM image you want to launch stored in your Openstack system. In this case, we 
  make use of the generated ID when you store your image in Openstack.
  

