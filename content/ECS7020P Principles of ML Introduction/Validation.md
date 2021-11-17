> models work together --> select the best family

- a family of models with random subsets of the data (learn different things)
- different models with random subsets of attributes (like [[#^648b6a|wrapping]])
- different family of models altogether
***
## Validation set approach
- ![[Screenshot 2021-11-16 at 10.09.01.png]]
	- result: error

## LOOCV: Leave-one-out cross-validation
- ![[Screenshot 2021-11-16 at 10.10.35.png]]
	- result: error.avg()

## k-fold cross-validation
> LOOCV is a special case of k-fold cross-validation, where k = N .
- ![[Screenshot 2021-11-16 at 10.12.08.png]]
	- result: error.avg()

***
## Bagging
- generate K sub-datasets by bootstrap
- train K simple base models with each sub-datasets
- combines the predictions of the base models by averaging or voting
	- an vote example: $f(x)=\sum fk(x)/K$ ![[Screenshot 2021-11-02 at 22.13.46.png]]
	``` mermaid
	flowchart LR
	A(data) --> B(extract dark data) --> C(fit a linear model) --> D(combine to a non-linear model)
	C -->|repeat| A
	```
***
## Random forests
- train many individual trees
- randomising the training samples and the predictors
- predictors: average the individual prediction
- +: great accuracy (than a single tree)
- -: expensive to train, harder to interpret (than a single tree)
### Tree
- to create pure leaves, otherwise the algorithm will confused: [[#^0ccc67|The XOR problem]]
	- leaf: one of the decision regions; result
	```mermaid
	graph TD
	A[Root: salary > S] -->B(Leaf: Bad)
	A --> C(Age > 40)
	C --> D(Leaf: neutral)
	C --> E(Leaf: good)
	```
- splits are axis-parallel
	- otherwise use [[Linear Classifier]]
### The XOR problem ^0ccc67
- ![[Screenshot 2021-11-02 at 22.25.45.png]]

***
## Boosting
- sequence: supply previous sample
- ![[Screenshot 2021-11-17 at 09.42.26.png]]![[Screenshot 2021-11-17 at 09.42.41.png]]
- 