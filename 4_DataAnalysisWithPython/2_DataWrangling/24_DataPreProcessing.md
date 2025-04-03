# Pre Processing Data in Python
Converting or mapping data from "raw" to a defined fomrat.

## Objectives
- Identify and handle missing values
- Data Formatting
- Data Normalization (Centering and Scaling)
- Data Binning:
    Creating bigger categories from a set of numerical values.
- Transform Categorical Values to Numeric Variables

## Methodology
Operations along columns, each column is a pd.Series.
```python
    df["column1"] = df["column1"] + 1 # It maps to every value of the column
```

### Dealing with missing values
Missing Value representation -> NaN, ?, 0 or just a blank cell

Options:
    - Check with the data collection source
    - Drop the missing vlaues
        - Drop the variable / Column -> Only if most of the data is missing
        - Drop the data entry / Row -> Only if the variable we want to predict is missing
    - Replace the missing values
        - Replace with the average of the column of similar datapoints (For numerical values)
        - Replace with the mode (For categorical values)
        - Replace it based in other functions
    - Leave as missing data

```python
    ...
    df.dropna(subset = ["column1"], axis=?, inplace="") # axis = 0 drops the ROW ; axis=1 drops the COLUMN

    
    df["column"].replace(missing_value, new_value)
    # Eg mean
    mean = df["column"].mean()
    df["column"].replace(np.nan, mean)
```
