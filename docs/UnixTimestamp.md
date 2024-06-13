# UnixTimestamp


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**seconds** | **int** |  | [optional] 

## Example

```python
from openapi_client.models.unix_timestamp import UnixTimestamp

# TODO update the JSON string below
json = "{}"
# create an instance of UnixTimestamp from a JSON string
unix_timestamp_instance = UnixTimestamp.from_json(json)
# print the JSON string representation of the object
print(UnixTimestamp.to_json())

# convert the object into a dict
unix_timestamp_dict = unix_timestamp_instance.to_dict()
# create an instance of UnixTimestamp from a dict
unix_timestamp_from_dict = UnixTimestamp.from_dict(unix_timestamp_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


