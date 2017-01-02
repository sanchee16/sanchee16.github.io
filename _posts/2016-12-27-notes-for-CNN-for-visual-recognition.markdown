---
layout: post
title:  "Notes for CNN for Visual Recognition!"
subtitle: "A Course by Stanford"
date:   2016-12-27 12:00:12
categories: [notes]
---

Lesson 2:

- Image Classification 
- Semantic Gap - Representation of image on computer as numbers
- Challenges are: 
	- Viewpoint Variation - Camera roatations lead to changes in brightness.
	- Illumination issues
	- Deformation 
	- Occlusion
	- Background Clutter
	- Intraclass Variation 
- Follow a data driven approach i.e. Collect dataset of images and labels, use ML algos to train an image 
classifier and evaluate classifier on test images. 
- Nearest Neighbour Classifier - Use Manhattan distance 
- Do more compute at train time but prediction should be constant time computation. 
- Aside - Approximate Nearest Neighbour (FLANN)
- Hyper-parameter - Distance, and the value of k for kNN
- Training data, validation data and training data set or Cross Validation 
- Linear Classification 
- NN can see, hear, translate, control and think.