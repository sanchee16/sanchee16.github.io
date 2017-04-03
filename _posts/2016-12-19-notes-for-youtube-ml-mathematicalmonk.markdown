---
layout: post
title:  "Notes for ML!"
subtitle: "A Course by Mathematical Monk's Channel(Youtube)"
date:   2017-03-19 11:45:34
categories: [notes]
---

Lesson 1:

- ML is algorithms for inferring unknowns from knowns. eg. Filtering out spam, Detect Handwriting, Face Detection, Speech Recognition, Netflix ranking, Navigation, Climate Modelling
- Classes of ML 
	- Supervised vs unsupervised Learning 
- Supervised Learning is given data $$(x_1, y_1), (x_2, y_2), (x_3, y_3), .............  (x_n, y_n)$$, choose a function f(x) = y where $$x_i$$ = data point and $$y_i = class/value $$ and then generalise for new values of x. i.e f(x) $$\to$$ y
- Two types of Supervised Learning problems 
	- Classification - $$y_i \in \{\text{finite set}\} $$. 
	- Regression -  $$y_i \in \{R\} $$ or $$y_i \in \{R^d\} $$.
- Unsupervised Learning is given data $$(x_1, x_2, x_3,........x_n)$$ i.e. $$x_i \in \{R^d\} $$
 Find patterns in data
	- Clustering
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