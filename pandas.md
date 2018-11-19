# Useful Pandas Snippets 


## Create a 'filled' date time index

```python 
dt_index = pd.date_range(start='11/06/2018', end='11/16/2018', freq='H')
date_df = pd.DataFrame(dt_index.date, columns=['date'])
date_df['hour'] = dt_index.hour
``` 
