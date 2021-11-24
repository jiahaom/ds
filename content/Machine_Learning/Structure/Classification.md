---
title: "Classification"
mathjax: true
---

> Know your metrics.

- use datasets to *obtain/estimate* the [[#^68e85f|Posterior Probabilities]] instead of *using*.
***
## Type
- [Linear_Classifier](content/Machine_Learning/Linear_Classifier.md): the simplest boundary
- [[content/Machine_Learning/Logistic_Model#^d37bff|Logistic Classifier]]: Approximated [[content/Machine_Learning/The_Bayes_Classifier#^68e85f|Posterior Probabilities]]
- [[K-Nearest]]: Approximated [[content/Machine_Learning/The_Bayes_Classifier#^68e85f|Posterior Probabilities]]
- [[content/Machine_Learning/The_Bayes_Classifier]]: True [[content/Machine_Learning/The_Bayes_Classifier#^68e85f|Posterior Probabilities]]
***
## Evaluation
[[content/Machine_Learning/Classification_Quality_Metric]]

***
- Shape of boundaries: Logistic regression and LDA build linear boundaries, QDA quadratic boundaries. kNN does not impose any particular shape.
- Stability: For a small number of samples, logistic regression can be very unstable, whereas LDA approaches produce stable solutions. 
- Outliers: Logistic regression is robust against samples which lie very far from the boundary, LDA and QDA can be affected. 
- Multi-class: Multi-class problems can be implemented easily in dicriminant analysis. 
- Prior knowledge: Can be easily incorporated following Bayesian approaches
