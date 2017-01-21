---
layout: post
title: Learning Notes-Structural Discovery
published: true
---

Unlike predictive analysis, structural discovery is to find the patterns of data.

## K-means
- **prcedures**
  
  + decide the number of clusters
  + find initial starting points - centroids (usually random)
  + label data points that close to a certain centroid as one cluster，e.g.,Cluster0 (use voronoi diagram)
  + refit the centroids in each cluster (e.g., Centroid A) in a certain cluster (in every coordinate, calculate the average value of all data points in that cluster） - the process called *convergence*
  + repeat until the centroids remain the same

- **key concepts**
  + cluster size
  + centroids
  + distortion
  + BiC/AIC

- **notes**

  1. how to determine the final clusters: with different initial centroids, the final clusters will differ.   
   + ramdonly try several initial starting points and get several restarts
   + use distortion(mean square deviation，Sum of Squares) to determine which restart works best. 
  2. how to determine the number of clusters: the distortion usually gets smaller along the increase of cluster size 
   + cross-validation doesn't work
   + BIC and AIC works ( Bayesian Information Criterion, Akaike Information Criterion) - compare how much fit would be spuriously expected from a randomized K centroids(do not move centroids) and how much fit we actually had
   + choose the cluster size with best value of AIC or BiC
  3. most importantly, scientific question matters!!!!

## advanced clustering algorithms

1. Gaussian Mixture Models - Expectation Maximization Algorithm
   - a centroid and a **radius** ( threshold)
   - Used during model calculation
   - Assess with distortion, AIC/Bic,  and **likelihood**
   - difference from K-means
     + clusters can overlap 
     + explicity treating points as outliers 
   + **key concepts** : cluster size, centroid, radius, distortion, BiC/AIC, likelihood
2. Spetral Clustering
3. Hierachical Clustering -> Hierachical Agglommerative Clustering
   + each data point starts as a cluster
   + two clusters are combined if the fit is better
   + continue until no more cluters can be combined
   
## factor analysis 
- **types**
  + experimental: get groups in bottom-up fashion, more educational data ming
  + confirmatory: test the goodness of existing structure, more psychometric
- **procedures**
  + algorithms: PAF(principal axis factoring), PCA(principal components analysis,more common)
   + first factor tries to find a combinition of variable-weightings that gets the best fit to the data
   + the second tries to fit the remaining unexplained variance....
   + factors are made ortogonal.
  + computer a factor score ( each factor can generate a linear euqation)
  + find variables strongly load on each factors(e.g, F1) and get the loading - many criteria 
  + generate one-factor-per-variable(scale) models by iteratively 
   - assigning each item to factors
   - dropping the one item that loads most poorly in one factor, if it has no strong loading (if every variable is strong loading, best!)
   - refitting factors 
   
  
- **key concepts**
  + goodness: 
   - rsquare( what propotion of the variance in the variables is explained by the factoring)
   - cross-validated rsquare
  + internal reliability of scales ( cronbach's α)

- **notes**
  1. Unlike clustering that groups data points together, factor analysis finds how group data features/variables together.(two problems can be trasformative, but not the same)
  2. the procedures deal with quantative variables, there is also a variant for categorical and binary data, **Latent Class Factor Analysis (LCFA --Magidson & Vermunt, 2001; Vermunt & Magidson,2004)**, as well as a variant for mixed data types, **Exponential Family Principal Component Analysis (EPCA – Collins et al., 2001)** 
  3. context matters!!! make reasonable variable selection.
  

## questions

- what is cross-validation?
- what is model calcuation? ( Expectation Maximization Algorithm)
- what is non-linear dimension-reduced space? what is dimensionality reduction? (spetral clustering)
- what is a support vector machine? ( spetral clustering)
- how to understand the mathematical mechanisms of factor analysis?


Baker, R.S. (2015) Big Data and Education. 2nd Edition. New York, NY: Teachers College, Columbia University.
