# Data Formatting
Data is stored by different people and that can mean different formats.
Bringing it to a common standard allows to make a meaningful comporation.

We must also check the data types of the columns to avoid strange behaviors later on.

```python
# Example: transform miles per galon to Liter per 100km
df["city-mpg"] = 235 / df["city-mpg"]
df.rename(columns={"city-mpg": "city-l100km"}, inplace=true)

# Show data type
dataframe.dtypes()

# Modify data type
dataframe = dataframe.astype(type)
``` 
