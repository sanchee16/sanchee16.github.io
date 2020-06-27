---
layout: post
title:  "Notes for Designing Data-Intensive Applications"
subtitle: "A Book by Martin Kleppmann"
date:   2020-06-22 10:00:12
tag: [Book, Notes, Tech]
---


Preface:
- Today is the day of buzz words - NoSQL, Big Data, Web-scale, Sharding, Eventual consistency, ACID, CAP theorem, Cloud services, MapReduce, Real-time 
- Driving forces for development in data related systems 
	- Huge scale needs efficient processing of traffic and data
	- Agility to test things quickly is really the key driver
	- Prallelism is going to increase
	- IaaS has revolitionised the cloud and everyone has ability to excute things no matter which part of the world you are in
- An application is data intensive if data is primary challenge in terms of quantity, complexity & speed of change
- Scalable, available, resilient and curosity
- Building for scale that you don’t need is wasted effort and may lock you into an inflexible design. In effect, it is a form of premature optimization. 

Foundations of data systems:

Chapter 1:
	- Reliability
		- Software failures & bugs
	- Scalability
		- Load, Performance, Latency & Throughput
	- Maintainability
		- Operability, simplicity & evolvability
	- Applications need common functionality like databases, caches, search and filter, stream processing & batch processing
