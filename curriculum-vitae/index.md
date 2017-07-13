---
layout: page
title: Curriculum Vitae
description: "My professional portfolio"
image:
  feature: 2-point_half.png
  credit: imgkid
  creditlink: http://imgkid.com/blue-tech-background.shtml
share: true
comments: false
---

## Profile

Telecommunication Engineer major in Distributed Systems with interest in information technology services. Distributed
Computing and large scale systems have become areas I really like to hear about. I am an
ambitious Software Engineer with great interest in new problems and challenges. That is why I show a proactive
personality where I always train myself in new trends and technologies improving my easiness to grasp technologies.

---

## Work Experience

### Software Developer                                                                        [June 2016 - Present]

**[iZettle AB](https://www.izettle.com/se)**

Currently working in the Tech department of iZettle in the platform team.
Working with Java, Dropwizard, Docker, InfluxDB, Grafana, Splunk, AWs,
Docker and Docker clustering technologies for Microservices. We also maintain
some critical systems in iZettle that make use of Postgres and Cassandra

### Software Developer                                                                        [February 2014 - June 2016]

**[Comeon! Stockholm AB](http://www.comeon.com/)**

During my time at Comeon! I was involved in multiple areas of the system
which included several accomplishments:
- Building a pipeline for multiple test environments based on Jenkins, Docker
& Kubernetes for distributed container management in Google Cloud.
This allowed to have immutable, isolated test environments
for our teams to test multiple features and automated tests in parallel
and remove the contention of teams working on one unique test environment.

- Design and implemenation of a microservice to migrate our KYC document storage.
Stack included a REST Stateless Webservice in Dropwizard with a replicated
MongoDB in GridFS clustering mode in replica sets.
In addition, the REST client was implemented with Netflix Hystrix;
integration test where setup to work with a mongo DB docker container.

- Tech talks given in the company regarding No SQL databases, Git and Gitlab (See talks section)
- Refactoring of legacy code in parts of the old payment web service API to adapt it
to the new frontend payment flow.
- Refactoring and clean of code architecture of mobile application based
in Angular JS.

Technologies used:

- ***Server side:*** Java programming with Servlets, Netflix Hystrix,
 Tomcat and REST services based on dropwizard.
- ***Frontend:*** JavaScript, Angular JS and JQuery.
- ***Data layer*** uses mainly MySQL, MongoDB.
- ***Testing*** includes Junit and Mockito for mocking.
- ***Version Control:*** migrated from SVN to git.
- ***Process and Tools:*** Maven & Jenkins, Kubernetes with docker.

### Research Engineer                                                                       [June 2013 - January 2014]

**[SICS-Swedish Institute of Computer Science	](http://www.sics.se/)**

**Total months:** (8 months)

**Technology:** Java, Maven, Glassfish, cloud technologies used like Amazon EC2 and Open Stack for prototyping and testing.

**_Accomplishments:_**

- Cluster management interface to allow provisioning a cluster through a web wizard from scratch.
-	Implementation of an interface to retrieve deployment progress of a cluster.
-	Bundling of an Amazon Machine Image (AMI) with our predefined software to increase the deployment speed.
-	Bundling of a Virtual Image for Open Stack to offer the same solution as Amazon EC2.
-	Orchestration development for deployment in Bare Metal physical machines.

### Master Thesis in SICS                                                                   [January 2013 - June 2013]

**[SICS-Swedish Institute of Computer Science	](http://www.sics.se/)**

**Total months:** (6 months)

**Thesis Work: KTHFS Orchestration – Platform as a Service orchestration for Hadoop.**

Design and implementation of a Domain Specific Language for cluster deployment platform to configure Hadoop clusters in
Amazon EC2 and Open Stack cloud infrastructures.

**_Supervisor: Dr. Jim Dowling, Examiner: Prof. Seif Haridi_**

<div markdown="0">
<a href="http://kth.diva-portal.org/smash/get/diva2:648868/FULLTEXT01.pdf" class="btn btn-info">Download the Thesis</a>
</div>

**_Accomplishments:_**

- Design orchestration architecture with jclouds, chef and YAML, implemented 2 artifacts based on this design:
	* Implemented a web portal using Java Server Faces with Primefaces that configures a web application with a monitoring application, KTHFS Dashboard.
	* Integrated orchestration architecture in KTHFS Dashboard that allows deployment of a Hadoop cluster with chef and jclouds from a cluster defined in a YAML file.
- Optimize the orchestration architecture, managed to reduce the deployment time by increasing the throughput through asynchronous Future constructs.

### Software Developer                                                         [July 2010 - February 2011]

**[GSI - Group of Intelligent Systems at ETSIT UPM.](http://www.gsi.dit.upm.es/en/)**

**Total months:** 9 months

**Technology:** Primarily Java programming and software development on this language

---

## Educational Background

### Degree Master of Science, Software Engineering of Distributed Systems (M.Sc.)                [August2011- June2013]
**[KTH – Royal Institute of Technology](http://www.kth.se/)**

**_Master student in parallel with my double degree studies which includes Swedish language courses._**

### Telecommunications Engineering (Equivalent to MSc level accredited by ABET/EAC)           [September 2005- June2013]
**[Technical University of Madrid (UPM)](http://www.etsit.upm.es/index.php/en/)**

**_Double Degree program KTH + UPM, Erasmus exchange program_**

---

## Certifications

- **Algorithms: Design and Analysis, part 1.** Coursera & Stanford University. March 2015.
- **Machine Learning.** Coursera & Stanford University. Summer 2014.
- **Functional Programming in Scala.** Coursera & EPFL. Nov 2013.

---

## Skills

<p> Since I like to work at all stack levels, I have a large variety of multidisciplinary technical skills which
includes:
</p>

- **Operating Systems:** Ubuntu, Windows
- **Frontend Technologies:** HTML, JavaScript (Competent), jQuery, Angular JS
- **Programming Technologies:** Java (Experienced), Go (Adv. Beginner),
Python (Adv. Beginner)
- **Cloud Technologies:** Amazon Web Services (Adv. Beginner), OpenStack Nova(Adv. Beginner)
- **Database Technologies:** MySQL(Competent), Cassandra(Adv. Beginner), Neo4j(Beginner), MongoDB(Competent)
- **Version Control:** Git, SVN
- **Scripting:** Bash scripting (Beginner)
- **Other:** Docker (Competent), Kubernetes (Competent), Ansible (Adv. Beginner)

---

## Open Source Contributions

Contributing to open source projects from SICS in relation to my old Master Thesis work and time at SICS.

- **Karamel:** Karamel orchestrates the execution of Chef Cookbooks using jClouds.
My contribution includes adding preliminary support to Openstack: [Project Link](https://github.com/karamelchef)

- **HOPS Hadoop:** Hadoop Open Platform-as-a-Service. [Project Link](https://github.com/karamelchef)

---

## Code Portfolio:

If you want to have a better view of my side projects, I recommend checking out my
[github account](https://github.com/alorlea/) as in here I will have a brief selection of the projects I felt most
proud of:

- **Distributed Monitor Service:** Implementation of a small web service in Python with Flask, Javascript and HTML.
The idea is to have a python agent monitoring the cpu usage of the nodes and send this information to this web
service to monitor them. [Code Link](https://github.com/alorlea/CPUMonitorService)

- **Campaign Optimizer:** Here we try to allocate in an optimal manner different campaign schedules so we can
maximize the revenue of showing this advertisements. This solution was implemented with a dynamic programming
algorithm for the unbounded knapsack problem with some optimizations from S. Mortello's Knapsack problems book. [Code
 Link](https://github.com/alorlea/CampaignRevenueSolver)

- **A distributed URL Shortener:** What does it need to devise a highly available, scalable and distributed URL
shortener? Here I try to implement a web service using Drop wizard in order to attain a service with the previous
requirements.
The architecture involved implemented a 3 tier layered application by splitting frontend, backend and
data in layers. Both frontend application and backend services where implemented. The solution was tested in Amazon
Web services using an initial deployment of 2 frontend servers, 3 backend servers behind a load balancer where
backend services communicated with Amazon Dynamo, a scalable high performance No SQL DB.
Later on, the solution was designed also to work with Cassandra and another test was done by deployment a 4 node
Cassandra cluster in Amazon.
  - [Code Link](https://github.com/alorlea/UrlShortener)
  - [Solution Documentation](https://www.dropbox.com/sh/agxa7xe383qhp1g/AACqGYsLugKc9PgOXkDWWCIRa?dl=0)

---

## Tech Talks

I have done multiple talks both internally at my workplace and as a IEEE Volunteer for students & young professionals.

- **Introduction to Distributed Data Processing:** Small presentation as an overview to present Spark, Hadoop and
Flink as a general picture of the different frameworks with special focus on examples and libraries for Apache Spark.
[Prezi Link Here](http://prezi.com/yhq_6l_cby39/?utm_campaign=share&utm_medium=copy&rc=ex0share)
- **Crash to No SQL:** Talk focusing on the No SQL ecosystem focusing on the different data models, CAP Theorem and
later on zooming on different database implementations like Cassandra, Riak or MongoDB.
[Prezi Link Here](http://prezi.com/yhq_6l_cby39/?utm_campaign=share&utm_medium=copy&rc=ex0share)
- **Apache Thrift and HTTP 2.0:** Informative talk for discussing on possible technologies that could be handy when
trying to communicate between our systems in frontend and backend.
[Google Slides Here](https://drive.google.com/open?id=112zFPVSTLVExHzhC_NLVIGDnTY6vONa-h7DqR_sN9X0&authuser=0)
- **Introduction to Git and Gitlab:** Presentation to show git and gitlab as a possible transition from SVN.
[Prezi Link Here](http://prezi.com/qoqisors8nha/?utm_campaign=share&utm_medium=copy&rc=ex0share)
- **Tech Interview Workshop:** Small presentation given to students in order to give them tips of how to prepare and
orientate their preparation for interviews in IT companies.

---

## Competitions

- **Judge IEEExtreme 10.0.** Design programming problems for IEEExtreme 24 hour online competition with 6500+ teams worldwide hosted by IEEE.
- **Judge IEEExtreme 9.0.** Design programming problems for IEEExtreme 24 hour online competition with 6500+ teams worldwide hosted by IEEE.
- **Judge and Quality Assessor IEEExtreme 8.0.** Design and evaluate programming problems for IEEExtreme 24 hour online competition with 6500+ teams worldwide hosted by IEEE.
- **Contestant of IEEExtreme.** Part of a 3 member team on multiple editions of IEEExtreme including 6.0, 4.0 and 3.0
. On the last edition our team managed to obtain a Wordwide ranking position 110 and Region 8 ranking position 40.

---

## Languages

- Spanish (Mother tongue).
- English (Second language, Professional Working Proficiency)
- Swedish (4 course levels from KTH, up to intermediate/advance level)
- French (Up to Secondary School)
