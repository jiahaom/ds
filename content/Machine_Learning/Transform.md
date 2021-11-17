---
title: "Transform"
mathjax: true
---

> change the way represent samples
- one of the most important: 
many ML models = a transformation + a simple model
> - extract features from each pic as training data. 
> - ![[Screenshot 2021-11-02 at 19.30.59.png]]
> -  if we extract 4 values, we need fewer training pics.
---

- can be either hand-crafted or trained.
- after training remain fixed.
---
- if we know how to transform: learn the model which operates on the destination space
- if we don't know: learn it by selecting or tuning; Kernel method
---
## Same Number of Dimensions
### Linear
#### PCA
- provide an importance score for each component / to each dimension of the destination space
	```mermaid
	flowchart LR
	A --> C
	A(10D) -->|PCA| B(10D)
	B(10D) -->|score| C(5D)
	```
- score:  ^3ea892
	- rank the attributes defining the destination space
	- remove the least important feature [[#^04faa5|feature selection]]
#### Rotation
- PCA + Rotation: ![[Screenshot 2021-11-02 at 20.21.52.png]]
#### Scaling
> - change the numerical values of one attribute
> - doesn't change the data, but some models produce different solutions: k-means

### Non-linear
- pipeline: ![[Screenshot 2021-11-02 at 20.28.56.png]]
	- non-linear transformation
	- linear classifiers
	- logical function
	- combine
		- example: ![[Screenshot 2021-11-02 at 20.29.50.png]]

---
## Dimensionality reduction
### Feature selection ^04faa5
> attributes usage < original
- assume only a subset of attributes are relevant
	- M attributes has 2^M - 1 subsets: [[#^d04556|example]] ^a08716
	- use target metric to evaluate how relevant
- use [[#^3ea892|score]] to select
	- need a model trained on each subset (to find the best)
- can be a validation
#### Filtering
- to find the score by fitting a model and obtaining its validation performance
	- consider each attribute individually
	- ex: attributes x1 and x2 do a poor job separately, but together reveal clear boundary. ![[Screenshot 2021-11-02 at 21.50.38.png]]
- simple, fast, but miss interactions.
	```mermaid
	flowchart LR
	A(X1) --> D(f1 = 10) --> G(selected)
	B(X2) --> E(f2 = 12) --> H(selected)
	C(X3) --> F(f3 = 7)
	```
#### Wrapping ^648b6a
> attributes usage < original
- if we suspect the interaction be crucial
	- train a model by different subsets of features
	- evaluate each model by using validation approaches
	- pick the highest validation performance one
- [[#^a08716|M attributes has 2^M - 1 subsets]]
	- x1, x2, x3: x1 | x2 | x3 | x1, x2 | x1, x3 | x2, x3 | x1, x2, x3| ^d04556
### Feature extraction
> attributes usage > original (produce new)