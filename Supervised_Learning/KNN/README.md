# K-Nearest-Neighbor algorithm  

The k-nn algorithm is a simple **supervised** machine learning algorithm that can be used both for classification and regression. It's an **instance-based** algorithm. So instead of estimating a model, it stores all training examples in memory and makes predictions using a similarity measure. 

Given an input example, the k-nn algorithm retrieves the k most similar instances from memory. Similarity is defined in terms of distance, that is, the training examples with the smallest (euclidean) distance to the input example are considered to be most similar.

The target value of the input example is computed as follows:  
  
Classification:  
a) unweighted: output the most common classification among the k-nearest neighbors  
b) weighted: sum up the weights of the k-nearest neighbors for each classification value, output classification with highest weight  
  
Regression:  
a) unweighted: output the average of the values of the k-nearest neighbors  
b) weighted: for all classification values,  sum up classification value$*$weight and divide the result trough the sum of all weights  

The weighted k-nn version is a refined version of the algorithm in which the contribution of each neighbor is *weighted* according to its distance to the query point. Below, we implement the basic unweighted version of the k-nn algorithm for the digits dataset from sklearn.


## Dataset

The digits dataset is a collection of 8x8 pixel images of hand-written digits (0-9). Each image is flattened into a 64-dimensional array to represent pixel intensities. 