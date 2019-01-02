## List files in a directory 

Imports: 
```python
from os import listdir
from os.path import isfile, join
```

List files: 
```python
files = [file for file in listdir(path) if isfile(join(path,f))]
```

