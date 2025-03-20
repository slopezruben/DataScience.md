# Data Description
After the data has been loaded, look at the data through pandas to gain basic insights

Data Types - Automatically infered from the data set
    pandas  -   py native
    object  -   string
    int64   -   int 
    float64 -   float
    datetime64,timedelta

```python
    import pandas as pd
    ...

    df.describe(include = all) # Full summary of statistics
    df.info() # top 30 rows + 30 bottom rows

    ...
```

