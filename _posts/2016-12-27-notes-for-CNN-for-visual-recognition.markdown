---
layout: post
title:  "Notes for CNN for Visual Recognition!"
subtitle: "A Course by Stanford"
date:   2017-03-06 12:00:12
categories: [notes]
---

Lesson 2:

- Image Classification 
- Semantic Gap - Representation of image on computer as numbers
- Challenges are: 
    - Viewpoint Variation - Camera rotations lead to changes in brightness.
    - Illumination issues
    - Deformation 
    - Occlusion
    - Background Clutter
    - Intraclass Variation 
- Follow a data-driven approach i.e. Collect dataset of images and labels, use ML algos to train an image 
classifier and evaluate classifier on test images. 
- Nearest Neighbour Classifier - Use Manhattan distance 
- Do more compute at train time but prediction should be constant time computation. 
- Aside - Approximate Nearest Neighbour (FLANN)
- Hyper-parameter - Distance, and the value of k for kNN
- Training data, validation data and training data set or Cross Validation 
- Linear Classification 
- NN can see, hear, translate, control and think.


Lecture 4:

- Forward pass gives loss and backward pass gives gradients
- Gradient Descent
    - Numerical which is slow and approx but easy to write
    - Analytical which is fast and exact but error prone
- Computational Graph is huge for Neural Turing Machine
- Chain rule for backprop
- Local gradients are computed at the time of forward pass and can be chained to global gradient later at the time of backprop.  
- For plus gate, during back prop, the value for the next gate is 1 * the previous value.
- For multiplicative gate, during back prop, the value for the next gate is the value of other input * the previous value. 
- Hence, add gate is gradient distributor, the max gate is gradient router and mul gate can be the gradient switcher.
- At branches, gradients are added according to multivariate chain rule.
- Graph class with nodes topologically sorted and forward and backward function
- Lot of memory required to store intermediate results that will be used during back prop
- For vectors, we have jacobian matrix which stores derivative of each element of output wrt input
- Vectorized Operations 
- Jacobian matrix is not always a full matrix and is a sparse matrix because there are values only on the diagonal and even not all those values are be used.
- Backpropagation is recursive application of chain rule along computational graph to computer gradients  of all inputs/params/intermediates
- Biological description of neurons 
    - Soma: cell body
    - Dendrites: listeners/input
    - Axon: terminals/output
- Activation functions 
    - Sigmoid 
    - tanh
    - ReLU
    - Maxout
    - Leaky ReLU
    - ELU
- Fully connected layer and hidden layers
- Kernel trick changes data representation to a space where it's linearly separable

