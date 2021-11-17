# The Bayes Classifier ^95fc31
- a classifier uses the True [[#^68e85f|Posterior Probabilities]]
- use odds ratio([[#^68e85f|Posterior Probabilities]] or [[#^555d72|Class Priors]]+[[#^3a3076|Class Densities]]) to achieves ***the highest accuracy*** by comparing: $\frac {P(y=red|x)}{P(y=blue|x)} = \frac {P(x|y=red)P(y=red)}{P(x|y=blue)P(y=blue)}$ ^839888
	- if >1 ==> y = red
	- if < 1 ==> y = blue
- a ideal classifier: we never know $\frac {P(y=red|x)}{P(y=blue|x)}$


***
> ![[Screenshot 2021-11-06 at 10.25.09.png]]

## Class Priors ^555d72
> - assume 70 % of the population y=red, 30% y=blue.
-  P(y=red) = 0.7, P(y=blue) = 0.3.

### Estimate
- use a dataset: $P(y=red) = \frac {N(red\ samples)}{N(samples)}$
***
## Class Densities ^3a3076
>- assume $\frac{1}{4}x = a, \frac{3}{4}x = b$ in the red example,  $\frac{2}{3}x = a, \frac{1}{3}x = b$ in the blue example
- $P(x=a|y=red) = \frac {1}{4}$
- $P(x=b|y=red) = \frac {3}{4}$
- $P(x=a|y=blue) = \frac {2}{3}$
- $P(x=b|y=blue) = \frac {1}{3}$
### Estimate
1. build class densities: [[Unsupervised Learning]]
2.  ## Gaussian Density
	### Discriminant Analysis
- we assume the class densities are Gaussian.
- one predictor:![[Screenshot 2021-11-06 at 11.45.17.png]]
	- parameters:  $µo$ is the mean and $σ^2o$
is variance of the Gaussian density.
![[Screenshot 2021-11-06 at 12.20.44.png]]
- K predictors:![[Screenshot 2021-11-06 at 11.46.48.png]]
	- parameters:  $µo$ is the mean and $Σo$ is  covariance matrix.
![[Screenshot 2021-11-06 at 12.23.47.png]]
- linear discriminant analysis (LDA)
	- If $Σblue= Σred$ ==> the boundary is linear. We call this scenario. 
	- ratio	 of the cost:![[Screenshot 2021-11-06 at 12.29.31.png]] ^4f4693
- quadratic discriminant analysis (QDA)
	- the boundary is quadratic

***
## Posterior Probabilities ^68e85f
- **Accuracy **
- $P(y=red|x)$
- $P(y=blue|x)$
> -* fallacy of the transposed conditional*: a confusion between [[#^3a3076|Class Densities]] and [[#^68e85f|Posterior Probabilities]]

### Bayes Rule
- $P(y=red|x) = \frac {P(x|y=red)P(y=red)}{p(x)}$ 
- $P(y=blue|x) = \frac {P(x|y=blue)P(y=blue)}{p(x)}$ 


# A Bayesian Extension ^a80775
[[ECS7020P Principles of ML Introduction/Classification Quality Metric]]


### Minimize the Cost
- ![[Screenshot 2021-11-06 at 14.54.56.png]]
- $T = \frac {C(blue)}{C(red)} = ratio\ of\ the\ cost = a\ threshold\ value = boundary$ [[#^4f4693]]

### Example
- 2 classes: blue and red.
	- $P(y=blue|x) = 0.1; P(y=red|x) = 0.9$
-  the cost of misclassifying a  sample:
	-  $C(blue)=\$5000; C(red)=\$20$
- The Bayesian Classifier would label $x$ as red, because of the expected cost:
	- $C(blue)*P(y=blue|x) = \$500$
	- $C(red)*P(y=red|x) = \$18$
