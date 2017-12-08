---
layout: post
title:  "Notes for CNN for Visual Recognition!"
subtitle: "A Course by Stanford"
date:   2017-10-09 10:00:12
tag: [notes]
---

Lesson 1:

- Today is age of images/video but image/video data is hard to use
- Computer Vision as an interdisciplinary field
- Eye as an inspiration for big bang of species
- Vision important for speciation in the early evolution of the species
- Mechanical Vision i.e. Camera models - Camera Obscura
- Hubel and Wiesel experiment
- Primary visual cortex is very far away from eye
- Simple structures excite neurons in human brain
- Block World models - Visual world simplified into basic geometrical shapes
- Book Vision by david marr
- Hierarchical Representation
- Generalized Cylinder and Pictorial Structure models
- Normalized Cut - perceptual grouping problem - image segmentation
- Real time Face Detection by Fuji Films Camera
- Major focus is recognition
- Engineered Features like SIFT, HOG
- Spatial pyramid matching for scene recognition
- Deformable Part Model
- PASCAL visual object challenge
- Imagenet
- Image classification really useful for making progress in other image machine learning problems like image detection, segmentation, image captioning
- Semantic Segmentation and Perceptual Grouping
- Tell a story given a scene


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


Lecture 7:

- CNN operate over volumes. 
- Filters are convolved over the image ie the filter is slid over the image spatially computing dot products which result in activation map.
- $$ \text{output_size} = ((N-F+2*P)/S) + 1 $$ where N is width/height, F is filter size, P is padding and S is stride.
- Input padding is a common practice since we want to preserve sizes spatially otherwise the size of the input decreases sharply.
- To always achieve same output volume spatially for stride of 1, use $$ (F-1)/2 $$ zero padding
- K, N, F and P are hyperparameters where K is the number of filters and is in powers of 2 as certains subroutines are efficient in computations with a power of 2.
- The depth of the output of a convolution will the total number of filters.
- With parameter sharing it introduces, $$F*F*D_1$$ weights per filter.
- 1*1 convolutions are important since they return the same sized output since we do dot products over the full depth of the volume (depth columns or fibres).
- The size of F is usually odd. 
- Usually, images are preprocessed to squares.
- The filter is also called kernel. Filters capture local information. 
- Along the depth of the output volume, all the neurons have actually looked at the same patch but their weights will still be different.
- Pooling layer makes the representations smaller and managable 
- Pooling operates over each activation map independently
- LeNet - 5 
- AlexnNet 
    - Use of ReLU
    - Used norm layers
    - Heavy data augmentation 
    - Dropout
- ZFNet 
- VGGNet
- GoogleNet
- ResNet
    - Skip Step
    - Batch normalization layer and hence can use a higher learning rate 
    - No dropout
    - Xavier/2 initialization 
    - Faster than VGGNet(20 layers) inspite of having 152 layers 
- Policy network
- As we go ahead with the architectures, we find that the numbers of parameters are reduced but more conputation is required and the results are too promising.
- Instead of fully connected layers, use average pooling layers in the end of a CNN.
- Convnets stack - CONV, POOL, Fully Connected layers
- Trend towards smaller filters and deeper networks and getting rid of POOL/FC layers


