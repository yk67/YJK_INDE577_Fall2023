# Ensemble Learning

## Introduction
Ensemble methods are machine learning techniques that involve combining multiple models to improve predictive performance. There are different types of ensemble methods, including bagging, random forest, and Adaboosting.

### Bagging
Bootstrap aggregating, or bagging, is a technique in which multiple models are trained on different subsets of the training data, which are randomly sampled with replacement. The predictions from the individual models are then combined to make a final prediction. Bagging can be used with any base model, such as decision trees, and is particularly useful when the base model is prone to overfitting.

### Random Forest
Random forest is an extension of bagging that uses decision trees as the base model. In addition to randomly sampling the training data, random forest also randomly selects a subset of features for each split in the decision tree. By combining the predictions from multiple decision trees that have been trained on different subsets of the data and features, random forest reduces overfitting and improves generalization performance.

### Boosting
Adaptive boosting, or Adaboosting, is a technique in which multiple models are trained sequentially, with each subsequent model focused on correcting the errors of the previous model. During training, the data points that are misclassified by the current model are given higher weights, so that the subsequent model is more likely to correctly classify those data points. The final prediction is a weighted combination of the predictions from all the models. Adaboosting is particularly useful for improving the performance of weak classifiers.

## Dataset
Customer_data from Kaggle. The category features are fea_1, fea_3, fea_5, fea_6, fea_7, fea_9.
Label 1 means the customer is in high credit risk and label 0 means the customer is in low credit risk.
