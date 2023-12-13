 # Logistic Regression
 [Logistic regression](https://en.wikipedia.org/wiki/Logistic_regression) is similar to [linear regression](/blog/ml-linear-regression/), but instead of predicting a continuous output, classifies training examples by a set of categories or labels.  For example, linear regression on a set of social and economic data might be used to predict a person's income, but logistic regression could be used to predict whether that person was married, had children, or had ever been arrested.  In a basic sense, logistic regression only answers questions that have yes / no answers, or questions that can be answered with a 1 or 0.  However, it can easily be [extended](https://en.wikipedia.org/wiki/Multinomial_logistic_regression) to problems where there are a larger set of categories.

**Assumptions:**

Logistic Regression models make a few assumptions:

-the dependent variable is binary, multinomial, or ordinal
-observations are independent (not from repeated measurements)
-little to no collinearity among the independent variables
-linearity of independent variables and log odds
-The success of the model depends on the sample size (usually requiring large sample sizes to achieve high accuracy)

# Dataset
Here, I'm using the [Wine](https://archive.ics.uci.edu/ml/datasets/Wine) dataset from UCI. It maps thirteen continuous variables representing chemical contents of a wine to three labels, each a different winery in Italy.
