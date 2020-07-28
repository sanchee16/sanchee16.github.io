---
layout: post
title:  "Notes for Building Microservices"
subtitle: "A Book by Sam Newman"
date: 2020-06-29 10:00:12
tag: [Book, Notes, Tech]
---


Preface:
- Microservices are an approach to distributed systems that promote the use of finely grained services with their own lifecycles, which collaborate together. Because micro‐ services are primarily modeled around business domains, they avoid the problems of traditional tiered architectures.
- It empowers autonomy, improves scaling.
- Infra, automation and CD can help but if the fundamental system design isn't good then there are limitations.
- Too many microservices is also a pain.

Microservices:
- Domain-Driven Design helped us understand the importance of representing the real world in our code, and showed us better ways to model our systems.
- CI has taught us how to treat every checkin as a candidate for release.
- Alistair Cockburn’s Hexagonal Architecture guided to layered arch where business layers could hide
- Netflix Antifragile Systems at Scale
- Microservices are small, autonomous services that work together.
	- Small focused on doing one thing well 
	- Cohesion is the drive to have related code grouped together
	- Single Responsibility Principle; Gather together those things that change for the same reason, and separate those things that change for different reasons.
	- How small is small ?
		- Number of lines isn't a great measure
		- Something that can be rewritten in 2 weeks
		- Small enough and no smaller
			- How well the service aligns to team structures
			- The benefits around interdependence increase and the downsides of having more and more parts start coming up
- Autonomous
	- Can you make a change to a service and deploy it by itself without changing anything else
- Key Benefits
	- SOA and distributed system
	- Tech heterogeneity to quickly absorb new tech 
		- Finding the right balance 
		- Netflix and Twitter, for example, mostly use the Java Virtual Machine (JVM) as a platform, as they have a very good understanding of the reliability and performance of that system
	- Resilience
		- Bulkhead: If one component of a system fails, but that failure doesn’t cascade, you can isolate the problem and the rest of the system can carry on working. Service boundary is the usual bulkhead
	- Scaling
		- With microservices, scaling can be done in isolation and on-demand. 
	- Ease of Deployment 
		- 





















