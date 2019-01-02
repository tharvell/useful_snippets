# Useful Pandas Snippets 


## Create a 'filled' date time index

```python 
dt_index = pd.date_range(start='11/06/2018', end='11/16/2018', freq='H')
date_df = pd.DataFrame(dt_index.date, columns=['date'])
date_df['hour'] = dt_index.hour
```

## Database like DataFrame merging 

```python 
pd.merge(left, right, how='inner', on=None, left_on=None, right_on=None,
         left_index=False, right_index=False, sort=True,
         suffixes=('_x', '_y'), copy=True, indicator=False,
         validate=None)
``` 

## Listing the column names

```python
list(my_dataframe.columns.values)
```
or
```python
list(my_dataframe)
```


## Changing some column names 

```python 
df = pd.DataFrame({"A": [1, 2, 3], "B": [4, 5, 6]})
df.rename(index=str, columns={"A": "a", "B": "c"})
```

## Conditionally change data in a specific column
This one is a little wierd due to the way pandas copys, so you need the iloc function

```python
df.loc[df['ConditonCol'] == something, ['ColToChange']] = 'NewValue'
```

Or another way to view the problem  

```python
# Mask is an array of True, False [True, True, ... False ... True, False]
mask = (df['CondCol1'] == something1) & (df['CondCol2'] > value1)
df.loc[mask, 'ColToChange'] = 'NewValue' 

``` 
