> Know your metrics.

- use datasets to *obtain/estimate* the [[#^68e85f|Posterior Probabilities]] instead of *using*.
***
## Type
- [[Linear Classifier]]: the simplest boundary
- [[Logistic Model#^d37bff|Logistic Classifier]]: Approximated [[The Bayes Classifier#^68e85f|Posterior Probabilities]]
- [[K-Nearest]]: Approximated [[The Bayes Classifier#^68e85f|Posterior Probabilities]]
- [[The Bayes Classifier]]: True [[The Bayes Classifier#^68e85f|Posterior Probabilities]]
***
## Evaluation
[[ECS7020P Principles of ML Introduction/Classification Quality Metric]]

***
- Shape of boundaries: Logistic regression and LDA build linear boundaries, QDA quadratic boundaries. kNN does not impose any particular shape.
- Stability: For a small number of samples, logistic regression can be very unstable, whereas LDA approaches produce stable solutions. 
- Outliers: Logistic regression is robust against samples which lie very far from the boundary, LDA and QDA can be affected. 
- Multi-class: Multi-class problems can be implemented easily in dicriminant analysis. 
- Prior knowledge: Can be easily incorporated following Bayesian approaches
