---
layout: post
title:  "Notes for Artificial Neural Networks!"
subtitle: "A Course by Hugo Larochelle"
date:   2016-10-21 11:45:34
categories: [notes]
---

Lesson 1:

- He defines the terminologies as weights denoted by w, bias denoted by b, activation function denoted by g(.), neuron preactivation(I/P) denoted by x, neuron activation(O/P) denoted by h(x). Everything exept b is a vector.
- He starts a discussion about potential activation functions in ANN.  
	- Linear Activation Function, g(a) = a, No squashing of I/P
 	- Sigmoid Function, g(a) = 1/(1+e^(-a)), Lies between 0 and 1, always +ve, bounded, strictly increasing.
 	- Tanh Function, g(a) = (e^(2a)-1)/(e^(2a)+1), Lies netween -1 and 1, bounded, strictly increasing
 	- ReLU Function, g(a) = max(0, a), Bounded below 0, Strictly increasing, tends to give neurons with sparse activities because it is 0 over a large range of -ve numbers.
- He further discusses the complexity of computations the neural network can perform. 
- He talks about linearly separable problems(binary classification problems) which have a decision boundary and use single neuron to perform logistic regression. This can be achieved using sigmoid.
- He goes further and talks about alternate representations of input vector which can convert the non lineraly separable problem into a separable one. For eg. XOR can be represented by AND(X^, Y) on x axis and AND(X, Y^) on y axis. He tries to break the problem into pieces and check if single piece of problem can be represented by a neuron or a group of neurons and then combine all the representations to generate a representation for non linearly separable problem.
- He discusses the hidden layer pre-activation, hidden layer activation and output layer activation for a single layer neural network. Going ahead with multilayer neural network, the only difference is that multilayer neural network has multiple hidden layers.
	- To perform binary classification, one can use sigmoid as output activation function. 
	- For multiclass classification one needs multiple outputs, so one uses conditional probablity 
	p(y = c|x) where c is the class and then using softmax activation function; A function which sums to 1 when all the probablities are added. Additionally, softmax is strictly positive.
- He discusses universal approximation throem i.e. a single layer hidden neural network with linear output unit which can approx. any continuous function arbitrarily well, given enough hidden units.
- He discusses the inspiration that neural networks draw from biological neurons and talks about the idea of different layers and how they work in parallel with the visual cortex. He uses edges and points to introduce the idea of complex shapes formed using these simple structures and uses face detection as an example. He defines the following terms too.
	- Action potential is an electrical impulse that travels through the axon. 
	- Firing rate of a neuron is frequency with which a neuron can spike.
	- Neurons tend to excite or inhibit other neurons.
- Analogy between artificial NN and biological NN
	- Activation function is analogous to firing rate.
	- Weights in ANN decide the excitation or inhibition of a neuron.
	- Activation function and bias model the action potential of a neuron. 
