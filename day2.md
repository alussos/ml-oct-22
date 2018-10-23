# Objectives
- Grok data visualization using Python
- Understand the internals of the blackboxes of common ML models
- Be able to actually build some models

# Agenda
0. [15] Classification vs Regression
0. [30] Linear Regression Review, Practice & Tuning
1. [30] Data Visualization
1. [15] Pandas warm up with breast cancer data set
2. [30] kNN Theory
3. [30] kNN Practice
3. [45] Logistic Theory and practice 
4. [30] Naive Bayes Theory
5. [30] Naive Bayes Practice
6. [45] Decision Trees, Bagging and Random Forests
7. [30] Tree Practice
8. [30] Unsupervised & clustering Theory
9. [30] Clustering Practice
10. [20] Open Q&A

# Datasets
- [Breast cancer data](https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/datasets/breast-cancer.csv)
- [Doctor visit data](https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/datasets/health_data.csv)
- [Twitter data](https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/datasets/clean_twitter_data.csv)
- [CC data](https://s3-us-west-2.amazonaws.com/simplefractal-teaching/cc_default.csv)

# [15] Classification vs Regression
- What's classification?
- What's regression?
- What are some applications?

# [30] Linear Regression Review, Practice & Tuning
- Brief review of the math
- Let's work with our housing data and build a linear model.
- R-squared and how to interpret (https://en.wikipedia.org/wiki/Coefficient_of_determination)
- Practice tuning it, use different columns
- Play with the different parameters
 
## Discussion
- When is this model useful?
- What are its limitations?

# [15] Pandas warm up with breast cancer dataset
- Read in the breast cancer data
- Do some EDA

# kNN Theory
- What is kNN?

## Worksheets
https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/worksheets/worksheet_1_kNN.pdf
https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/worksheets/worksheet_3_kNN.pdf

## Discussion
- What are the pros and cons of this model?
- How/where might it fail?

## Practice
- Let's build a kNN classifier on the breast cancer dataset.
- Now you tune it and see how good you can make it.

# Logistic Regression
- What's the theory?
- What does it optimize for?
- What are the assumptions?
- Pros and cons?

## Exercise 
- Build a logistic regression on the breastcancer data
- Tune the parameters
- Let's interpret the results

# Naive Bayes
- Why is it called naive?
- How does it work?

## Worksheets
- https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/worksheets/Worksheet_1_conditional_probability_univariate.pdf
- https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/worksheets/Worksheet_2_conditional_probability_multivariate.pdf


## Exercise
- Let's build it on the breastcancer data
- How does it compare to Logistic?

## Mini NLP Lab
Let's use twitter data.

# Trees, Bagging and Forests
- Non-linearity
- Boolean logic
- Binary cuts

# Break to answer surveys

## Worksheets
- https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/worksheets/Decision+Trees/DT_wksht_2.pdf
- https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/worksheets/Decision+Trees/DT_wksht_3.pdf

Let's apply it to the breast cancer data.

## Regression Worksheets
- https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/worksheets/Trees+Continued/trees_continued_wksht_1.pdf
- https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/worksheets/Trees+Continued/trees_continued_wksht_3.pdf

Let's apply it to Boston Housing Data

## Bagging
- Why are trees unstable?
- Ensemble methods...
- https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/worksheets/Decision+Trees/DT_wksht_4.pdf

## Discussion
Read https://elitedatascience.com/bias-variance-tradeoff
Let's discuss together.

## Random Forest
- The procedure
- An intuitive example: https://www.quora.com/How-does-randomization-in-a-random-forest-work/answer/Edwin-Chen-1?share=1&srid=h5QG

Practice RF on breast cancer data.

## Optional Lab
Let's practice on CC Data.

# Unsupervised & Clustering
## K-means
- How does it work?
- How do we know if a cluster is "good" or not? You may not like the answer...

## Procedure
Assume K clusters, with unknown centers c1, ..., ck, each of which is a p-dimensional vector.

A good measure of how good a cluster is is the sum of squared distances of the points to the center of that cluster. Then we'll sum that over all the clusters to see how good our choice of centers were.

We want to minimize the sum over all the clusters of the sum of square distances of points to the center of the cluster they belong to.

It's difficult to minimize this analytically, so we'll need an algorithm to help us do this.

K-means does this iteratively by the following:

1. Initialize the centers c1, ..., ck to be arbitrary, distinct points from the dataset.
2. Choose the optimal assignment of points to clusters given by the centers above. Call this assignment of points to centers A. We do this by assigning each point to the center nearest to it.
3. Now that the assignment is fixed, choose the optimal centers for that assignment A.
4. Repeat 2 and 3 until convergence, a.k.a. the assignments don't change on subsequent iterations.

## Question
Why would the scaling of the data matter?

## Practice
Disregard the class label and cluster the breast cancer data.
