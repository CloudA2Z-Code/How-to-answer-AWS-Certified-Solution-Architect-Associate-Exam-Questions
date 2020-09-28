
Question 1:
==========
You are the Solutions Architect for a health insurance service company that wants to start building and supporting IoT devices for patients who recently signed new clauses in the contract. This will open opportunities to expand its market but also introduces some restrictions. All services and data involved have to guarantee HIPAA compliance and include in-transit encryption. Due to high sensitivity data, bypassing the internet is crucial. The architecture uses already ELBs. They want to avoid DNS re-configuration and IP address caching when it comes to the IoT devices. What combination of services may be the closest option to address this challenge?

Answer:
=======

What (Observations - Understand the question)
---------------------------------------------
AWS technologies 
-----------------
* AWS global Accelerator
* AWS ELBs
* AWS IoTs

Questions highlighted
----------------------
* High sensitive data or compliance
* Avoid DNS reconfiguration or lesser infra or network changes.
* IoT devices


How ( How well this scenario can be dealt, can use of below AWS technology will help ?)
---------------------------------------------------------------------------------------
* AWS Global Accelerator
* Route 53
* Private Link

Why - Analyse the questions and answer this scenario based question.
--------------------------------------------------------------------
Service Capabilities:
---------------------
* AWS Global Accelerator - AWS Global Accelerator is a service that improves the availability and performance of your applications with local or global users. It provides static IP addresses that act as a fixed entry point to your application endpoints in a single or multiple AWS Regions, such as your **Application Load Balancers, Network Load Balancers or Amazon EC2 instances**.
