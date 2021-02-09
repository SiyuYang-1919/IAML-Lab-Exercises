## 1. Maximum Likelihood Estimation
- In statistics, maximum likelihood estimation (MLE) is a method of estimating the parameters of a probability distribution by maximizing a likelihood function, so that under the assumed statistical model the observed data is most probable. 
- The idea is to transfer solving the density function directly to solveing parameters for the Likelihood Function (the product of univariate density function with unknown parameters to be solved for independent and identically distributed random variables).
- The general likelihood function:
$$ L(\theta) = f(x_1,...,x_n|\theta) = \prod_{i=1}^n f(x_i|\theta) $$
$$ ln(L(\theta)) = ln(\underset{\theta} {\textrm{arg max}} \prod_{i=1}^n f(x_i|\theta)) $$
, where
$$ \theta = {\theta_1, \theta_2,..., \theta_s} $$
To solve $\theta$, we write the partial derivatives for each parameters and let them equal to 0, then solve the parameters.
- ```Why we use 'log': ```
![alt text](https://img-blog.csdn.net/2018041616140618)
When $a$ in ${log_a}()$ is greater than 1, the $x$ can be limitlessly large when the slope $k$ equals 0, that is, when the slope $k = 0$, $y$ can get its maximum value.
- ```Examples in Naive Bayes classifier:```
There are two applications of MLE in Naive Bayes:
  1) Estimation of priori probabilities $p(C_k)$; 2) Estimation of conditional probabilities $p(X|C_k)$.