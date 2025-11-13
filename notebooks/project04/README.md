# 🚢 Project 4 – Predicting a Continuous Target with Regression (Titanic)

**Author:** Albert Kabore  
**Date:** November 2025  

##  Objective  
This project applies **machine learning regression techniques** to predict *fare* — the amount a passenger paid for the Titanic voyage — based on demographic and travel-related features.  
Building upon earlier classification work (predicting survival), this notebook explores continuous target prediction using:  

- Linear Regression  
- Ridge Regression (L2 Regularization)  
- Elastic Net Regression (combined L1 + L2)  
- Polynomial Regression (Non-linear fit)  

The goal is to identify which features most strongly influence fare, evaluate each model’s performance, and interpret trade-offs between simplicity and accuracy.  

---

##  Libraries Used
```python
import seaborn as sns
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression, Ridge, ElasticNet
from sklearn.preprocessing import PolynomialFeatures
from sklearn.metrics import mean_squared_error, mean_absolute_error, r2_score
```

## Visualizations

Polynomial Regression: Pclass vs Fare
Shows non-linear fare distribution across passenger classes.

Higher Order Polynomial (Comparison Plot)
Demonstrates that degree 5 offers no improvement over degree 3 while increasing model complexity.

(All plots generated using Matplotlib and displayed within the notebook.)

### Section 5.5 Reflection (Bullet Summary)

The degree-5 polynomial did not improve accuracy over the cubic model.

Both captured the same non-linear fare pattern across classes.

Evaluation metrics were virtually identical.

Higher degree increased complexity and potential overfitting.

The cubic model achieved a good balance between simplicity and predictive power.

Passenger class (pclass) remained the dominant predictor of fare.

### Section 6 – Final Thoughts & Insights

## 6.1 Summarize Findings
