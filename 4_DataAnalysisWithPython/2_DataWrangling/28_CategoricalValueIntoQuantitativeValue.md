# Turning categorical value into qualitative variables
Since most statistical models can't take strings or objects as input,
it is necessary to turn this values into some sort of numerical format.

## Solutions
Dummy variables for one categorial variable.

```python
pd.getDummies(df['fuel`]) # if fuel can be gas or diesel, creates the columns gas and diesel and assigns 1 or 0 depending of the type
``` 
