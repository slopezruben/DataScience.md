# Analysis of Variance (ANOVA)
Analyze a categorical variable and see the correlation between different categories of it.

Returns:
    - F-test score: ratio of variation between the groups mean
        - Smaller F means less correlation
    - p-value: significancy

In a bar chart, we can see the difference between the values of different categories of variables,
but with ANOVA, we can quantify this difference instead of depend on intuition.

```python
    df_anova=[['make', 'price']]
    grouped_anova=df_anova.groupby(["make"])

    anova_results = stats.f_oneway(grouped_anova.get_group("honda")["price"], grouped_anova.get_group("subaru")["price"])
    # A F-test value < 1 and a p-value > 0.05 indicate no significant difference

    anova_results = stats.f_oneway(grouped_anova.get_group("honda")["price"], grouped_anova.get_group("jaguar")["price"])
```
