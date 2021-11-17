## Accuracy
[[ECS7020P Principles of ML Introduction/Regression Quality Metric#^e51d1f]]
- [[KNN]] and [[Logistic Model#^bbc977|Logistic Regression]] don't have!
***
## Error Rate
[[ECS7020P Principles of ML Introduction/Regression Quality Metric#^9d4269]]
- [[KNN]] and [[Logistic Model#^bbc977|Logistic Regression]] don't have!
***
## [[The Bayes Classifier#^a80775|A Bayesian Extension]]
> if 1 patient in 1000 people, we say all people are healthy, the accuracy is 99.9%.

## Confusion Matrix
- to see how classifier treat each class individually
### Counting
- ![[Screenshot 2021-11-06 at 15.10.46.png]]
 - 3 red samples are misclassified as blue
### Rate
-  when working with imbalanced datasets, counts might be misleading
- ![[Screenshot 2021-11-06 at 15.13.09.png]]
### Detection problems
![[Screenshot 2021-11-06 at 15.22.37.png]]
- $Accuracy = \frac {TP+TN}{N(examples)}$
- $Error = \frac {FP+FN}{N(examples)} = 1 - Accuracy$
#### Quality Metrics
- Sensitivity / TPR / Recall
	- $\frac {TP}{TP+FN}$
- Specificity / TNR
	 - $\frac {TN}{(TN+FP)}$
 - Precision / Positive Predictive Value
	 - $\frac {TP}{(TP+FP)}$

### Optimization
> it's difficult to improve 1+ quality metrics at the same time ==> consider pairs of them

1. Sensitivity & Specificity
- The ROC Plane
![[Screenshot 2021-11-06 at 20.52.03.png]]
	- top left corner is the best: $Sensitivity = 	Specificity = 1$
	- can't rank classifiers based on them, but can filter classifiers.
-  The AUC
	-  area under the curve: a measure of goodness for a classifier that can be calibrated
	-  ![[Screenshot 2021-11-07 at 21.40.20.png]]
2. Precision & Recall
- $F1 = 2 * \frac {Precision*Recall}{Precision+Recall}$




