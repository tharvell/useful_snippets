# List objects in a bucket

```python
import boto3

s3_client = boto3.client('s3')
all_objects = s3_client.list_objects(Bucket = 'bucket-name') 
```


# CSV From S3 to DataFrame

``` python
import boto3
from io import BytesIO

data_obj = s3_client.get_object(Bucket='bucket-name', 
                    Key=r'file_name.csv') 

data_bytes = data_obj['Body'].read()

stream_string = BytesIO(data_bytes)

df=pd.read_csv(stream_string, encoding='latin-1', low_memory=False)
```
