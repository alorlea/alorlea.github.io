---
layout: post
title: Apache Hadoop & Flink automation in OpenStack with Karamel
modified:
categories: open-source
description:
tags: [Karamel, Openstack, Apache Hadoop, Chef, Automation, Apache Flink]
image:
  feature:
  credit:
  creditlink:
comments: true
share: true
published: true
date: 2016-04-10T17:26:30+01:00
---

This is a special post as it remarks my first contribution to a small open-source project and also to my ex-colleagues 
during my brief time at [SICS](https://www.sics.se/). 
 
This project is called [Karamel](http://www.karamel.io/). Karamel is 
a tool that simplifies big data deployments on a selection of cloud providers like AWS and Google Cloud Engine, 
in addition to baremetal cluster setups. It is quite easy to get started, you simply need to define your cluster in a 
file, submit it to the application and do one click!

With this tool you can easily have al big data cluster up and running in 
a few clicks which will have preinstalled hadoop , Apache Flink or even Apache Spark.
In addition, it is the preferred tool for testing out a new hadoop distribution named [Hops](http://www.hops.io/) 
which try to address the challenges and issues you could face when you work with very large scale hadoop clusters (for 
example, how to achieve [high availability of the namenode](http://www.hops.io/?q=content/hdfs))

# Deploying Clusters with Karamel

In the rest of this article, I will describe the process of creating a simple cluster running apache Flink in order to 
make a deployment using Karamel towards an Openstack environment. We will also go over how you can write a cluster file
 to be deployed using this tool and how you need to configure the Karamel in order to communicate with your cluster.

## Before we start

In order to deploy our Hadoop cluster on Openstack, first we will need to get a copy of the latest version of 
Karamel, you can do it [here](http://www.karamel.io/?q=content/getting-started-karamel). Here you will find 
guidelines to get started with other providers like AWS. You may download one of the available versions that have 
support for Openstack (version 0.2.0 onwards should do it) or download the source code and build the application with
 maven.
 
# Working with Karamel

Getting started with Karamel is quite easy, before launching our cluster, we will need to define the configuration of a
cluster. In a cluster definition file, we can identify 4 core elements to describe you cluster: **_Provider_**, 
**_Cookbooks_**, **_Attributes_** and **_Groups_**. 

In order to understand the role of each core component, we will go through a simple example cluster, let's imagine 
that I want to deploy a simple Hadoop cluster with Apache Flink running a namenode and 20 datanodes using an 
Openstack Infrastructure. 

So how can I express this information in Karamel? In addition, if we want to deploy a 
wordcount job when the cluster is ready, how can we achieve this? How can Karamel allow us to express this business 
needs? This is how you would do it, as shown on the following file: 

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

In this cluster, we can see 3 different code blocks gathering all the information we need for Karamel to satisfy our 
cluster needs. 


## Provider

The first segment of the file contains the provider specific information, for Openstack; we make use of the
  keyword nova in order to tell Karamel that this is an Openstack cluster and we are going to make use of the Openstack 
  Nova Controller. 

  After the keyword nova, it follows key parameters that Openstack will make use to deplou the necessary resources to
   run our software on.
  
  * __Flavor:__ This corresponds to a specific hardware configuration for the VM, this is similar to Amazon's EC2 
  instance descriptors. Openstack refers to them as flavors and each one specifies a configuration (CPU, RAM) and are
   not the same for everyone, as these are configured by the needs of the organization. To simplify this, Karamel makes
    use of the flavor id attached to your VM configuration.
   
  * __Image:__ This corresponds to the VM image you want to launch stored in your Openstack system. In this case, we 
  make use of the generated ID when you store your image in your Openstack project.
  
## Cookbooks
  
  The following code block, gathers the software that we will want to install on our nodes. For this purpose, 
  Karamel makes use of Chef Cookbooks that get will be processed on the nodes by running Chef Solo. To simplify the 
  transfer of the Cookbooks, they should be accessible by the application through Git so it can clone them and 
  execute the recipes on the nodes.
  
  For this example, we want to install Apache Hadoop and Apache Flink so we indicate this Karamel by the keyword 
  Cookbook and specifying the repositories where our Cookbooks are stored plus the branch we want to checkout.

## Groups

Under the groups sections, we define the cluster structure around groups 
of components and services. Here, we specify the number of nodes and the
recipes that will install the services to run on those nodes.

# Summary

In this, blog post we went over roughly how Karamel now has support to deploy
clusters in Openstack based infrastructures. This gives you the opportunity
to play with hadoop, flink or spark directly in your private cloud reducing the
time you need to configure a whole cluster.
