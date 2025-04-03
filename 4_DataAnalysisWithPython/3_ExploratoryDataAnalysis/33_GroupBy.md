# GroupBy
Assume you want to compare the information of the dataset by a categorical variable 
of it to analyze how other variables are affected by it.

In order to do that, use the groupBy method. 
```python
# Analyzing how drive-wheels and body style of vehicles are affected by price 
df_test = df[['drive-wheels','body-style','price']]
# This creates a DataFrame with the mean price of car by drive-wheels and body-style 
df_grp = df_test.groupby(['drive-wheels', 'body-style'], as_index=False).mean()

# Not really comprehensible, so we use the Pivot Method (Le da el formato excel)
df_pivot = df_grp.pivot(index='drive-wheels', columns='body-style')

# o podemos crear un heat map
plt.pcolor(df_pivot, cmap='RdBu')
plt.colorbar()
plt.show()

```

