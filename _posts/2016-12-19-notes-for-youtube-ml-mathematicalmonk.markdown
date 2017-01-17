---
layout: post
title:  "Notes for ML!"
subtitle: "A Course by Mathematical Monk's Channel(Youtube)"
date:   2016-12-19 11:45:34
categories: [notes]
---

Lesson 1:

- ML is algorithms for inferring unknowns from knowns. eg. Filtering out spam, Detect Handwriting, Face Detection, Speech Recognition etc.
- Supervised Learning is given data (x1, y1), (x2, y2), (x3, y3), .............  (xn, yn) , choose a function f(x) = y where xi = data point and yi = class/value and then generalise for new values of x.
- Two types of Supervised Learning problems 
	- Classification - yi is from some finite set. 
	- Regression - yi are from Real values.
- Unsupervised Learning is given data (x1, x2, x3,........xn)
	- Custering
	- Density Estimation
	- Dimensionality Reduction should project it down preserving the structure of data.
- Variations on supervised and unsupervised learning 
	- Semi Supervised Learning - (x1, y1), (x2, y2), (x3, y3), .............  (xk, yk), xk+1, xk+2 ....xn,
	predict yk+1, yk+2 ..... yn. eg. 
	- Active Learning 
	- Decision Theory
	- Reinforcement Learning - maximize overall reward and minimize overall losses.
- Generative vs Discriminative Models 
	- Discriminative = P(y given x) which is Conditional Probability
	- Generative = P(x and y) = f(x given y) p(y) = p(y given x) f(x) - models joint distribution - more powerful than Discriminative since using more parameters
	- Estimating a density is difficult and need a lot of data leading to high variance and hence Generative model will have bad performance than Discriminative.
- kNN 
	- circle concept that is used to decide the class of the test point
	- Probabilistic interpretation - (y) 
	- Discriminative model
	- Bias - variance tradeoff  