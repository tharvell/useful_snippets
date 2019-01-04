# Some useful funcitons for exploratory data analysis 

## Quick column information 
```python
def eda_column_info(df, col_name):
    """
    TODO: Doc String
    """

    value_counts_no_nan = df[col_name].value_counts()
    
    if value_counts_no_nan.max() <= 1:
        most_frequent_value = 'column of uniques'
        highest_frequency = 1
        nan_count = df[col_name].value_counts(dropna=False).loc[np.NaN]
        unique_value_count = len(value_counts_no_nan)
        return {
                "most_frequent_value":most_frequent_value,
                "unique_value_count":unique_value_count,
                "highest_frequency":highest_frequency,
                "nan_count":nan_count,
                "col_name":col_name,
            
                }
        
    
    
    
    most_frequent_value = value_counts_no_nan.idxmax()
    highest_frequency = value_counts_no_nan.loc[idxmax]
    nan_count = df[col_name].value_counts(dropna=False).loc[np.NaN]
    unique_value_count = len(value_counts_no_nan)
    return {
            "most_frequent_value":most_frequent_value,
            "unique_value_count":unique_value_count,
            "highest_frequency":highest_frequency,
            "nan_count":nan_count,
            "col_name":col_name
           }
    
```

