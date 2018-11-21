# Python Regular Expressions

# Quick Example

```python
pat = re.compile(r'\d-\{7}')
match = pat.search(folder_name)
if match: 
    return match.group()
``` 




