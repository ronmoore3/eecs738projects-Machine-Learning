# Probably Interesting Data

### By Ronald Moore and Austin Adams

#### Purpose
The purpose of this project is to show how machine learning algorithms can be used to model distributions on features within the dataset.

#### EM Algorithm Implementation
For this project, the Expectation Maximization (EM) algorithm was implemented in order to construct univariate Gaussian mixture models for the various features of a given dataset.

The EM algorithm has is composed of two parts, the expectation step (E-step) and the maximization step (M-step)
Given N random samples and k Gaussian components,
##### E-Step
* give some initial values of the parameters mu_k, sigma_k, and pi_k for each of the k Gaussian components
* for each k Gaussian component, calculate the value of the latent variable lat_i for all N samples
##### M-Step
* update the values of mu_k, sig_k, and pi_k for each of the the k Gaussian components

#### Discussion
* It is worthwhile to note that the success, computational speed (number of iterations), and parameter values (mu, sigma, mixing coefficients) of the EM all depend on the initial values of the parameters mu, sigma, and the mixing coefficient
* The EM algorithm seems to work better with continuous values rather than discrete values

#### References:
http://statweb.stanford.edu/~tibs/stat315a/LECTURES/em.pdf \
https://www.geeksforgeeks.org/gaussian-mixture-model/
