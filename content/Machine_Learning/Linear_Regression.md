---
title: "Linear_Regression"
mathjax: true
---

### The best linear model for training data: 
- [[content/Machine_Learning/Regression_Quality_Metric#^d91d7e|The least squares]]
## Simple Linear Regression
- $f(x) = w_0+w_1x$

- $\hat y =  f(x_i)= w^TX = w_0+w_1x_i$ ^b14eb7
	- one predictor: x
		- $X=[1,x_i]^T$
	- one label: y
	- use a dataset to tune two parameters to achieve the highest quality
		- $w = [w_0, w_1]$
		- $w_0: intercept$
		- $w_1: slope$
***

## Multiple Linear Regression
- $\hat y = f(x_i) = w^Tx_i = w0+w_1x_{i,1} +...+w_Kx_{i,K}$
	- $w=[w_o,w_1,...,w_k]$
	- predictors:
		- $x_i=[1,x_{i,1},x_{i,2}, ...,x_{i,K}]^T$
		- k-th predictor of the i-th sample
- e.g. build a linear model that maps age and height to salary:  ![[Screenshot 2021-11-15 at 11.47.06.png]]
-	$
\begin{equation*}
X = 
\begin{bmatrix}
1 & 18 & 175 \\
1 & 37 & 180 \\
1 & 66 & 158 \\
1 & 25 & 168
\end{bmatrix}
\end{equation*}$, $
\begin{equation*}
y = 
\begin{bmatrix}
12000 \\
68000 \\
80000 \\
45000
\end{bmatrix}
\end{equation*}$

***
## Simple Polynomial Regression
- $f(x_i) = w^TX=w_0+w_1x_i+w_2x_i^2+w_3xi^3=$
	- $X = φ_i = [1, x_i, x_i^2, x_i^3]^T$
	- $w^TX = w^Tφ_i$ 
