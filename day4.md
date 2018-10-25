# Objectives
- [60 min] Clustering theory (K-means, hierarchical)
- [60 min] Clustering practice
- [30 min] working with categorical data
- [30 min] (Today or tomorrow) Work on time series data
- [60 min] Supervised learning model recap

# Datasets
- Iris dataset
- Census data https://archive.ics.uci.edu/ml/datasets/Census+Income, https://archive.ics.uci.edu/ml/machine-learning-databases/adult/adult.data
- [CRX data](http://archive.ics.uci.edu/ml/machine-learning-databases/credit-screening/crx.data)

# Clustering
- What is it?
- Brainstorm examples...

## K means theory
Assume K clusters, with *unknown* centers c<sub>1</sub>, ..., c<sub>k</sub>, each of which is a p-dimensional vector.

A good measure of how good a cluster is is the sum of squared distances of the points to the center of that cluster. Then we'll sum that over all the clusters to see how good our choice of centers were.

We want to minimize the sum over all the clusters of the sum of square distances of points to the center of the cluster they belong to.

It's difficult to minimize this analytically, so we'll need an algorithm to help us do this.

K-means does this iteratively by the following:

1. Initialize the centers c<sub>1</sub>, ..., c<sub>k</sub> to be arbitrary, distinct points from the dataset.
2. Choose the optimal assignment of points to clusters given by the centers above. Call this assignment of points to centers A. We do this by assigning each point to the center nearest to it.
3. Now that the assignment is fixed, choose the optimal centers for that assignment A.
4. Repeat 2 and 3 until convergence, a.k.a. the assignments don't change on subsequent iterations.

Side Note 1: This alternating minimization in steps 2 and 3 is a special case of the Expectation Maximization (EM) algorithm.

Side Note 2: The above algorithm is called Lloyd's algorithm.

### Terms
- intra-cluster variation
- inter-cluster variation
 - WCSS (inertia)

## K means practice
- Let's practice on the Iris dataset and visualize http://scikit-learn.org/stable/auto_examples/datasets/plot_iris_dataset.html


## Hierarchical theory
Unlike K-means, we do not specify how many clusters we want. In the end, we have a tree-like representation of the data.

There are different kind sof hierarchical clustering, but we will focus on the most common kind: *bottom up* (a.k.a. agglomerative) hierarchical clustering.

We build a hierarchy in a "bottom-up" fashion.

## Procedure
1. Start with each point in its own cluster
2. Identify the two closest clusters and merge them.
3. Repeat step 2 until all points are in a single cluster.

Once we've constructed the tree of clusters from the bottom-up, we can cut it off at a certain height to get the number of clusters we desire. The lower we cut the tree, the more clusters we get.

## How to determine closeness of two clusters

Given two clusters A and B, we want to compute the dissimilarity between them, called *linkage*. There a couple of ways we can do this:

- Complete: compare all pairwise dissimilarities between points in A and B and take the maximum of these dissimilaritys to be the linkage.
- Single: Same as complete, except we take the minimum of these dissimilarities to be the linkage.
- Average: We take the avergae of the pairwise dissimilarities..
- Centroid: Dissimilarity between the centroid of cluster A and the centroid of cluster B.

Note that above, we will often use Euclidean distance as the measure of dissimilarity. An alternative is correlation-based distance, which is a measure of how correlated the features of two separate observations are.

## K means vs Hierarchical

## Clustering practice
- Practice 1: http://nbviewer.jupyter.org/gist/suneel0101/b9bcfcc3b75202112341
- Practice 2: http://nbviewer.jupyter.org/gist/suneel0101/39e2804783ff5a7c6e71

## In-depth practice with categorical variables...

# Supervised learning model recap (Part 1)
## Naive Bayes
1. What kind of input (categorical/continuous) does the Naive Bayes classifier take?
2. Can the Naive Bayes classifier do multi-class classification?
3. What does the 'Bayes' in Naive Bayes refer to?
4. What does the 'Naive' in Naive refer to?
5. When should we use Naive Bayes?
6. When should we definitely NOT use Naive Bayes?
7. How does Naive Bayes do with high dimensionality?
8. Does this classifier give us an interpretable probability?
9. What parameters can we tune, if any?

## Logistic Regression
0. What is the equation for logistic regression?
1. What kind of input does Logistic take?
2. Can it handle high dimensional input?
3. What is regularization and what is it for?
4. When should we regularize?
6. Does this classifier give us an interpretable probability?
7. What parameters can we tune?

## k Nearest Neighbors
0. What does the k in k Nearest Neighbors refer to?
1. If k is too, high what can happen?
2. Should we scale our features? What happens if we don't?
3. When should we use k Nearest Neighbors?
4. When should we definitely NOT use k Nearest Neighbors?
5. Can k Nearest Neighbors handle high dimensionality?
6. Given a k-neighborhood of points from different classes, say A, B and C, how do we decide which class wins in that neighborhood?
7. What are some ways that we can weight the votes? Why would we want to do so?
8. What parameters can we tune?
9. Do we get an interpretable probability?