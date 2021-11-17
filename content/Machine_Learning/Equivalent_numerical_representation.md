---
title: "Equivalent_numerical_representation"
mathjax: true
---

> - different units: miles vs km
> - incommensurable: weight vs height
> - different dynamic ranges: cm vs km 
- outlier sensitive: an outlier 10 times larger than the 2nd will squeeze min-max to [0, 0.1]
- quality guarantee on pipeline instead of these models.

## Min-max normalization
> - $z = \frac {x - min(x)}{max(x) - min(x)}$
> -  0 <= z <= 1
> - min(x) and max(x) are used during test and deployment
## Standardization
> - $z = \frac {x - \mu}{\sigma}$
> - mean = 0, unit standard deviation.