# The Value of Knowledge
![[985DCBB1-0DD1-4752-9504-81CCE2A02E6A.jpeg]]

# The Truth
- [[Sampling#^41ffae|Dataset]] != [[Sampling#^d1148e|Population]]
- no [[Sampling#^d1148e|Population]] in the ML
	- no True Performance
	- no absolute 
	- no best
	- random: different datasets/ performance ^ccf020

# 1. [[Training]]
- fit a model to dataset
# 2. [[Optimisation]]
# 3. [[ECS7020P Principles of ML Introduction/Validation]]
- find the best mode
# 4. [[Testing]]
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
- [[Equivalent numerical representation]]
2.  [[Transform]]
3.  Models
- several models running in parallel.
- must be trained using data.
4. [[Validation]]
5. Output
