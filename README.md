# Linear Regression

## 1. Introduction

Linear regression is a method to predict the expectation result/target (Y) based on an initial model and a sample feature (X) that we have. The initial models are called coefficient/slope (m) and intercept (b). This relationship can be written as Equation 1 below

$
Y = mX + b
$

which means, that X is the independent variable and Y is the dependent variable have a linear relationship. If the X increase then the Y increase too. To do this, we have to calculate the coefficient and intercept values first. The calculation of these values can be used by the Gradient Descent algorithm. The Gradient Descent algorithm is estimated from the Cost Function or Error Function. The coefficient and intercept will be obtained when the Cost Function reaches the minimum value through the number of iterations. The Cost Function itself can be written as Equation 2 below

**Cost Function**

$
MSE = {1 \over N} \Sigma_{i=1}^{n} (y_i - (mx_i + b))^2
$

where MSE is Mean Square Error and N is number of samples/data.

To calculate the change of coefficient (m) and intercept (b) for each iteration, we take the first partial derivative of the Cost Function equation. Then, the first partial derivative for m and b can be written

**Gradient Descent**

$
{df \over dm} = {1 \over N} \Sigma -2x_i(y_i - (mx_i + b))
$

$
{df \over db} = {1 \over N} \Sigma -2(y_i - (mx_i + b))
$

Then update the m and b

$
m = m - \frac{df}{dm} . \alpha
$

$
b = b - \frac{df}{db} . \alpha
$

where the $\alpha$ is the learning rate or step size for each iteration. If alpha is small, it makes the gradient descent move smoothly. In this algorithm, the $\alpha$ and number of iterations are adjusted to 0.01 and 10000 respectively.

## 2. Contact
:email: auliakhalqillah.mail@gmail.com

## References:

- https://ml-cheatsheet.readthedocs.io/en/latest/linear_regression.html#cost-function
- https://www.statisticshowto.com/probability-and-statistics/regression-analysis/find-a-linear-regression-equation/