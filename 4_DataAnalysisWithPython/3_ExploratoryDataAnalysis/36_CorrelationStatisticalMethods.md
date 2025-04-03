# Correlation Statistical Methods
To measure the strength of the correlation between continuous numerical variables is the Pearson Correlation.

## Correlation Coeficient
- 0  - No correlation
- -1 - Negative correlation
- 1  - positive correlatoin
## p-value: Certainty
- < 0.001   - Strong
- < 0.05    - Moderate
- < 0.1     - Weak
- > 0.1     - None


```python
# SciPy stats package
pearson_coef, p_value = stats.pearsonr(df['horsepower'], df['price'])
```
