
Question 1:
==========
You are the Solutions Architect for a health insurance service company that wants to start building and supporting IoT devices for patients who recently signed new clauses in the contract. This will open opportunities to expand its market but also introduces some restrictions. All services and data involved have to guarantee HIPAA compliance and include in-transit encryption. Due to high sensitivity data, bypassing the internet is crucial. The architecture uses already ELBs. They want to avoid DNS re-configuration and IP address caching when it comes to the IoT devices. What combination of services may be the closest option to address this challenge?

Answer:
=======

1 - What (Observations - Understand the question)
================================================
Used AWS technologies 
---------------------
* AWS global Accelerator
* AWS ELBs(Works at Layer 4 i.e. NLB and can cater traffic only within a AWS region)
* AWS IoTs

Questions/Pain areas highlighted
--------------------------------
* High sensitive data or compliance
* Avoid DNS reconfiguration or lesser infra or network changes.
* IoT devices


2 - How (How well this scenario can be architected, which AWS services can help)
================================================================================
* AWS Global Accelerator
* Route 53
* Private Link

3 - Why (Analyse the AWS services capability)
=============================================
Service Capabilities:
---------------------
* AWS Global Accelerator - AWS Global Accelerator is a service that improves the availability and performance of your applications with local or global users. It provides static IP addresses that act as a fixed entry point to your application endpoints in a single or multiple AWS Regions, such as your **Application Load Balancers, Network Load Balancers or Amazon EC2 instances**.

Compatibility:
-------------
Application Load Balancers, Network Load Balancers or Amazon EC2 instances

Scenarios you can use:
----------------------
1) Reduce Latency, Improve Performance & Increase Availability (Fact- By directing your traffic from user to application via AWS backbone on TCP and UDP based Traffic)
2) Can redirect traffic from an unhealthy service to healthy in < 30 secs. 
3) You can distribute proportion of traffic across endpoints using weighted traffic mechanism.
4) Works at Layer 7 (Unless ELB you can route traffic across AWS regions)
4) NoN Http workloads i.e. Gaming apps(UDP), IoT(MQTT or Voip)
5) HttP applications also supported - Need static IP (AnyCast Static IP to route the traffic inside the AWS networking backbone)

Check out more facts at AWS website: https://aws.amazon.com/global-accelerator/faqs/
