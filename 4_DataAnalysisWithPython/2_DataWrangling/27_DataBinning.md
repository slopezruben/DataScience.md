# Binning
Group values into bins, ex:
    age 0-120 -> [0 to 5], [6 to 10]
    price x -> [0-3000 ] -> cheap, ...

```python
    bins = np.linspace(min(df["price"], max(df["price"]), 4) # min, max, n_intervals
    group_names = ["Low", "Medium", "High"]
    df["price-binned"] = pd.cut(df["price"], bins, labels = group_name, include_lowest = True)
```

This allows to utilize histograms to plot the data in ranges.
