---
layout: post
title: Prediction Model- Regression

---
The post is a preview for week 2 educational data mining class. Regression analysis itself covers more things and requires more effort to learn. 


### Usage of Prediction Models

- predict a single variable in the dataset using other variables. 
- predict the future.
- make inferences from the present 

### component of regression

- the dataset used to build a regression model: each value  of the predicted variable in the dataset is called **a  training label**, associated with the traning lable is called a **set of features**.  with out the training lables, the model still exists. 
- regressors(predictors) + predicted variable 


### procedures 

- transfrom
  + unitization
  + using others transform functions, e.g., sqrt(x)

### caveat (warning)
 
a regression model: y = 4 + 2*x - 0.1x^2

In this case, it does not mean that x^2 is negatively correlated with y. We need to think it in a big picture, in this case, it means that when including x in the model, the relationship between x^2 and y becames negative. 

When the regressors in the model are not independent, we need to be more careful. 

### regression trees 

- non-linear (RepTree) : if x> 4, y=5, else if y=2
- linear (M5 prime, M5') : if x>4, y=2A+B, else if y=3A+3B

