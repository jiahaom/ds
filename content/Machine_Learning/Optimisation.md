---
title: "Optimisation"
mathjax: true
---

> find the best model if we have:
> - a collection of candidate models
> - quality metric 
> - ideal description of the target population

## Gradient Descent ^e433dc

- update iteratively / parameter tuning
- $w_{new} = w_{old}-\epsilon ∇E(w_{old})$ 
	- $w: model$
	- $\epsilon: learning\ rate/step\ size$
	- $∇E(w_{old}): slope$
		- large: overshoot
		- small: slow
-  initial model $w$ is crucial
	- usually chosen randomly
- stopping strategy 
	- Gradient Descent will not reach the optimal model
		- Number of iterations.
		- Processing time. 
		- Error value. 
		- Relative change of the error value.

### [[content/Machine_Learning/Regression_Quality_Metric#^d91d7e|MMSE: the best/lowest MSE for training data]] ^bab8a8

- [[content/Machine_Learning/Linear_Regression#^b14eb7|Linear Model]]:
	- $\hat y = Xw$
- [[content/Machine_Learning/Regression_Quality_Metric#^a03fa6|E_MSE]]:
		- $E_{MSE}(w) = \frac{1}{N}(y-\hat y)^T(y-\hat y)$
		= $E_{MSE}(w) =\frac{1}{N}(y-Xw)^T(y-Xw)$
	- the resulting gradient of the MSE is:
		- $assume:\bigtriangledown E_{MSE}(w) = \frac{-2}{N}X^T(y-Xw) = 0$
			-  $w =(X^TX)^{-1}X^Ty$
### [[content/Machine_Learning/Training#^10ee42|Training]]
- ![[Screenshot 2021-11-16 at 09.36.33.png]]
#### Data Size
- Batch gradient descent: whole training dataset. 
- Stochastic gradient descent: randomly, one sample. 
- Mini-batch gradient descent: a small subset from the training dataset.

### Optimisation
- Momentum
- RMSProp
- Adam


