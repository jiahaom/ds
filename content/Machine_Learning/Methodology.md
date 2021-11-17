---
title: "Methodology"
mathjax: true
---

# The Value of Knowledge
![[985DCBB1-0DD1-4752-9504-81CCE2A02E6A.jpeg]]

# The Truth
- [[Sampling#^41ffae|Dataset]] != [[Sampling#^d1148e|Population]]
- no [[Sampling#^d1148e|Population]] in the ML
	- no True Performance
	- no absolute 
	- no best
	- random: different datasets/ performance ^ccf020

# 1. [[content/Machine_Learning/Training]]
- fit a model to dataset
# 2. [[content/Machine_Learning/Optimisation]]
# 3. [[content/Machine_Learning/Validation]]
- find the best mode
# 4. [[content/Machine_Learning/Testing]]
- verify the model


***

> Don't let appearances fool you!
> - kg vs cm
> - y = 3 + 100Xa + 20Xb
> - linearly separable


# Pipeline
![[Screenshot 2021-11-02 at 19.24.48.png]]
- to avoid overfitting, we need more than original data as training data.
	- ![[Screenshot 2021-11-02 at 19.30.11.png]]
	- if we have a pic contains 3 x A x B values (3: RGB, A x B: number of pixels), we need more than 3 x A x B pics. (too many)
1. Data
- [[content/Machine_Learning/Equivalent_numerical_representation]]
2.  [[content/Machine_Learning/Transform]]
3.  Models
- several models running in parallel.
- must be trained using data.
4. [[content/Machine_Learning/Validation]]
5. Output
