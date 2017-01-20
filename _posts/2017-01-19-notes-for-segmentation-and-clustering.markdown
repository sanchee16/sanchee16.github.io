---
layout: post
title:  "Notes for Segmentation and Clustering!"
subtitle: "A Course by Udacity"
date:   2017-01-19 11:45:34
categories: [notes]
---

Lesson 1:

- Process of Segmentation 
- Standardisation where we treat a group as a whole
- Localisation where we treat them as individuals
- Grouping or binning
- It becomes difficult to group as the number of variables increase
- Clustering is a mathematical procedure for multidimensional analysis
- For a given set of objects, this procedure groups similar objects into clusters 
- Distance is way to measure similarity
- Intra-cluster separation is minimised and inter-cluster distance is maximised
- eg. Fraudulent insurance Claim, User Segmentation, Bioinformatics Study, Education
- Supervised and Unsupervised Learning 

Lesson 2:
- Selecting data based on objectives
- Use demographic and social data in first phases and remove historical data. 
- Predetermined Bias in Transactional Data - A/B testing
- Data types in clustering 
    - Continuous or Ordinal Variables
    - Outliers 
- Scaling data because distance is important in cluster analysis 
    - Z score or standard score i.e. no. of SD away from the mean
    - Unit interval compressing all values between 0 and 1
- Transforming Variables and visualising the data

Lesson 3:
- Variable Reduction Procedures help in accounting for most of the variables 
 in all of the observed variables 
- Principle variables or artificial variables explain most of the variance
- Try to use variable reduction when variables are somewhat related
- Need to weight benefits one can get from reducing the no. of variables used in 
 clustering analysis, with the all important aspect of needing to be able to explain
 the basis for clusters
- Types of Variable Reduction Procedures
    - Factor Analysis - Correlation between variables, trying to figure out causes 
    - Principal Component Analysis - accounts for total variation, trying to summarise
- Factor Analysis makes assumptions for underlying causal model while PCA doesn't
- In PCA, combine variables that are related to a common story
- Loadings and Values
    - Close to zero loading has less value on components