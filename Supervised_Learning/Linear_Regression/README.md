 # Linear Regression
 

In linear regression we want to model the relationship between a **scalar dependent variable** $y$ and one or more **independent (predictor) variables** $\boldsymbol{x}$.

**Given:** 
- Dataset $D = \{(\pmb{x}^{(1)}, y^{(1)}), ..., (\pmb{x}^{(m)}, y^{(m)})\}$
- With $\pmb{x}^{(i)}$ being a $d-$dimensional vector $\pmb{x}^{(i)} = (x^{(i)}_1, ..., x^{(i)}_d)$ and
- $y^{(i)}$ being a scalar target variable

**Assumptions:**
- We assume that dataset was produced by some unknown function $f$ which maps features $\pmb{x}$ to labels $y$
- We further assume that the labels $y^{(i)}$ are *noisy*
- In other words: the labels have been produced by adding some noise $\epsilon$ to the true function value: $y^{(i)} = f(\pmb{x}^{(i)}) + \epsilon$

**Model:**   
The linear regression model can be interpreted as a very **simple neural network:**
- It has a real-valued weight vector $\pmb{w}= (w_{1}, ..., w_{d})$
- It has a real-valued bias $b$
- It uses the identity function as its activation function
- Note: in most books the parameter vector $\pmb{w}$ is denoted in a more general form, namely as $\pmb{\theta}$

<img src="figures/linear_regression.jpg" alt="Drawing" style="width: 500px;"/>

**Approach:**   
Our goal is to learn the underlying function $f$ such that we can predict function values at new input locations. In linear regression, we model $f$ using a *linear combination* of the input features:

$$
\begin{split}
y^{(i)} &= b + w_1 x_1^{(i)} + w_2 x_2^{(i)} + ... + w_d x_d^{(i)} \\
&= \sum_{j=1}^{d} b + w_j x_j^{(i)} \\
&= \pmb{w}^T \pmb{x}^{(i)} + b
\end{split}
$$


 
# This file includes :  

 - Loading, manipulating and plotting data using numpy and matplotlib
 - The hypothesis and cost functions for linear regression
 - Gradient descent with one variable and multiple variables
 - Feature scaling and normalization
 - Vectorization and the normal equation
 - Linear regression and gradient descent in Tensorflow

# Dataset
In this post, I'm using the [UCI Bike Sharing Data Set](https://archive.ics.uci.edu/ml/datasets/Bike+Sharing+Dataset).
