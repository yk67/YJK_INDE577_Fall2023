
# The Perceptron Learning Algorithm

The __Perceptron__ learning algorithm a supervised learning algorithm for classification, and is credited as the first neural network. 

In this module, we implement the Perceptron learning algorithm for binary species classification using the [Iris data set](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_iris.html#sklearn.datasets.load_iris). 

Using two features, the Perceptron learning algorithm seeks a linear separator for the two species, if one exists. The algorithm proceeds as follows:

1. The species are labeled $1$ or $-1$.


2. For each instance, an Activation function is used to calculate a label prediction, $\hat{y}$. In this module, we use the __Sign Step Function__:

$$\hat{y}^{i} = \text{sign}(w^T\bar{x}^{i}) = \{1 \ \text{if} \ w^T\bar{x}^{i} > 0 , \ 0 \ \text{otherwise}\},$$ 
where:

- w = the vector of connection weights, which is initialized as a random vector
- x^i = the $i^{th}$ feature


3. For each instance, the loss is calculated as follows:

$$ L = \sum_{i = 1}^N (\hat{y}^i - y^i)^2,$$ 
where:

- $N$ = the number of instances
- $\hat{y}^i$ = the $i^{th}$ predicted label
- $y^i$ = the $i^{th}$ actual label


4. For each instance, an update is calculated as follows (called the Perceptron Update Rule), which we then iterate over:

$$ w^{i + 1} = w^i - \alpha (\hat{y}^i - y^i) \bar{x^i},$$ 
where: $\alpha$ = the learning rate.

Note that this update rule reduces the overall error! For every wrong prediction outputted, the algorithm "corrects" the prediction from the last incorrect guess. For example, if $\hat{y}^{i} = 1$ but $y^i = -1$, we would have $w^{\top} \bar{x} > 0$, thus $sign(w_{i + 1}^{\top} \bar{x^i}) = -1$. Similarly, if $\hat{y}^{i} = -1$ but $y^i = 1$, we would have $w^{\top} \bar{x} < 0$, thus $sign(w_{i + 1}^{\top} \bar{x^i}) = 1$. However, if the right prediction is outputted, i.e. either $\hat{y}^i = y^i = 1$ or $\hat{y}^i = y^i = -1$, the update rule yields $w_{i + 1} = w_i$ as desired.


5. The linear separator is given by:

$$ z = -\frac{w_1 x + w_3}{w_2},$$
where: $w = \begin{bmatrix} w_1 \\ w_2 \\ w_3 \end{bmatrix}$.



This algorithm is similar to Stochastic Gradient Descent, which we use in another module called the Multilayer Perceptron. 

---

The following libraries are required to run the attached code:

* [Matplotlib](https://matplotlib.org/)
* [Pandas](https://pandas.pydata.org/)
* [Numpy](https://numpy.org/)
* [Sklearn](https://scikit-learn.org/stable/)

