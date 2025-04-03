# Data Normalization
Making ranges consistent between variables allows a fairer comparison between different features.
Normalization can also make some statistical analyisis easier down the road.

For example, if we have to features, age (range 0 - 100) and income (0 - 20000), due to income having
a bigger range and value, it will make income to weigh more heavily. If we normalize the range (0 - 1),
it allow for fairer comparision between the two of them.

## How to

1. Simple feature scaling:  xnew = xold / xmax
```python
    df["length"] = df["length"] / df["length"].max()
```
2. minmax                   xnew = (xold - xmin) / (xmax - xmin)

```python
    df["length"] = (df["length"] - df["length"].min()) / (df["length"].max() - df["length"].min())
```

3. z-score                  xnew = (xold - average) / standard deviation 
```python
    df["length"] = (df["length"] - df["length"].mean()) / df["length"].std()
```
