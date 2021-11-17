---
title: "Regression Quality Metric"
mathjax: true
---
- think it before build it
***
- embrace the error
	- no precise input data 
	- no perfect solution
	- therefore, represent this discrepancy as:
		- $y = \hat{y}+e  = f(x)+e$
- find association between attributes instead of causation
- build relationship instead of causal models

# Error ^9d4269

$E = \frac {N(incorrect\ samples)}{N(samples)}$
***
## Estimate mean squared error/ MSE ^a03fa6

> ![[Pasted image 20211006162907.png]] 
- find the minimum MSE:
	- ![[Pasted image 20211006163329.png]]

### The least squares ^d91d7e

[[Machine_Learning/Optimisation#^bab8a8|MMSE: the best model for training data]]
- might not be the best model during deployment
- $w =(X^TX)^{-1}X^Ty$
	-	$X: design\ matrix$
	-	$y: label\ vector$



***
#### Root mean squared error/ RMSE
-  ![[Pasted image 20211006202945.png]]
- measures the sample standard deviation of the prediction error.

#### Mean absolute error/ MAE
- ![[Pasted image 20211006203032.png]]
- measures the average of the absolute prediction error.

#### R-squared/ R
- ![[Pasted image 20211006203136.png]]
-  measures the proportion of the variance in the response that is predictable from the predictors.
***
# Flexibility
- the ability to capture the complexity of the underlying pattern
- related to the number of parameters, interpretability and accuracy (trade-off)	

## Interpretability
- the ability to describe what's going on / understand how a predictor is mapped to a label
 - more Inflexible, simpler and easier to interpret.
## Accuracy ^e51d1f
- more flexible, less error
- $A = \frac {N(correct\ samples)}{N(samples)}$
# Generalisation
- the ability to make good predictions / successful deployment.
	- assessed by comparing training and deployment performance:![[Pasted image 20211006204358.png]]
	- training [[#^a03fa6|MSE]] & deployment [[#^a03fa6|MSE]]
	- overfitting & underfitting & just right
