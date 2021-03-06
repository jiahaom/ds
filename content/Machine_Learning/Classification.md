---
title: "Classification"
mathjax: true
---

> Know your metrics.

- use datasets to *obtain/estimate* the (#^68e85f|Posterior Probabilities.md) instead of *using*.
***
## Type
- [Linear_Classifier](/Machine_Learning/Linear_Classifier.md): the simplest boundary
- [Logistic Classifier](/Machine_Learning/Logistic_Model.md): Approximated [Posterior Probabilities](/Machine_Learning/The_Bayes_Classifier.md)
- K-Nearest.md: Approximated [Posterior Probabilities](/Machine_Learning/The_Bayes_Classifier.md)
- (/Machine_Learning/The_Bayes_Classifier.md): True [Posterior Probabilities](/Machine_Learning/The_Bayes_Classifier.md)
***
## Evaluation
[Classification_Quality_Metric](/Machine_Learning/Classification_Quality_Metric.md)

***
- Shape of boundaries: Logistic regression and LDA build linear boundaries, QDA quadratic boundaries. kNN does not impose any particular shape.
- Stability: For a small number of samples, logistic regression can be very unstable, whereas LDA approaches produce stable solutions. 
- Outliers: Logistic regression is robust against samples which lie very far from the boundary, LDA and QDA can be affected. 
- Multi-class: Multi-class problems can be implemented easily in dicriminant analysis. 
- Prior knowledge: Can be easily incorporated following Bayesian approaches
