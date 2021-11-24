---
title: "Logistic_Model"
mathjax: true
---


## Classifier

^d37bff

-  $p(distance)=\frac{e^d}{1+e^d} = \frac{1}{1+e^{−d}}$
- ![](/Machine_Learning/pics/Screenshot%202021-11-16%20at%2021.30.48.png)
	- $p(0) = 0.5$
	- $As\ d → ∞,\ p(d) → 1$
	- $As\ d → −∞,\ p(d) → 0$

- if we set the distance between boundary and sample: $d = w^Tx_i$
	> - d: label ![](/Machine_Learning/pics/Screenshot%202021-11-16%20at%2022.36.17.png)
	- logistic function: $p(d) = \frac {e^{w^Tx_i}}{1+e^{w^Tx_i}}$	


## Regression ^bbc977
- $L= \prod_{y=red} (1 − p(x_i)) \prod_{y=blue} p(x_i) = 0$
### [Regression_Quality_Metric](/Machine_Learning/Regression_Quality_Metric.md)
- doesn't use accuracy and error rate!
- likelihood function: $l= \sum_{y=red} log[(1 − p(x_i)]+\sum_{y=blue} log[p(x_i)] = 0$
- to tune/ find maximizes L or l: [Gradient_Descent](/Machine_Learning/Optimisation.md)

-e.g. 
- $p(0) = 0.5, p(1) ≈ 0.73, p(2) ≈ 0.88, p(−1) ≈ 0.27, p(−2) ≈ 0.12  ![](/Machine_Learning/pics/Screenshot%202021-11-16%20at%2022.54.45.png)

	- $d(triangle) = 2, d(square)=-2$
	- $p(triangle) ≈ 0.88, 1 − p(square) ≈ 0.88$ 
	- $L = p(triangle) (1 − p(square)) ≈ 0.77$
