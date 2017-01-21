---
published: true
---

## Structural Discovery
Unlike predictive analysis, structural discovery is to find the patterns of data.

### K-means
- **prcedures**
  
  + decide the number of clusters
  + find initial starting points - centroids (usually random)
  + label data points that close to a certain centroid as one cluster，e.g.,Cluster0 (use voronoi diagram)
  + refit the centroids in each cluster (e.g., Centroid A) in a certain cluster (in every coordinate, calculate the average value of all data points in that cluster） - the process called *convergence*
  + repeat until the centroids remain the same

- **notes**

  1. how to determine the final clusters: with different initial centroids, the final clusters will differ.   
   + ramdonly try several initial starting points and get several restarts
   + use distortion(mean square deviation，Sum of Squares) to determine which restart works best. 
  2. how to determine the number of clusters: the distortion usually gets smaller along the increase of cluster size 
   + cross-validation doesn't work
   + BIC and AIC works ( Bayesian Information Criterion, Akaike Information Criterion) - compare how much fit would be spuriously expected from a randomized K centroids(do not move centroids) and how much fit we actually had
   + choose the cluster size with best value of AIC or BiC
  3. most importantly, scientific question matters!!!!

### advanced clustering algorithms

1. Gaussian Mixture Models - Expectation Maximization Algorithm
   + a centroid and a **radius** ( threshold)
   + Used during model calculation
   + Assess with distortion, AIC/Bic,  and **likelihood**
   + difference from K-means
    + clusters can overlap 
    + explicity treating points as outliers 
2. Spetral Clustering
3. Hierachical Clustering -> Hierachical Agglommerative Clustering
  + each data point starts as a cluster
  + two clusters are combined if the fit is better
  + continue until no more cluters can be combined
  
### factor analysis 

- find how data features/variables together

### questions

- what is cross-validation?
- what is model calcuation? ( Expectation Maximization Algorithm)
- what is non-linear dimension-reduced space? what is dimensionality reduction? (spetral clustering)
- what is a support vector machine? ( spetral clustering)