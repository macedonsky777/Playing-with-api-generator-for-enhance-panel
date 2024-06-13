# ProcessInfo


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**pid** | **int** |  | 
**name** | **str** |  | 
**cpu_usage** | **float** |  | 
**res_memory** | **int** |  | 

## Example

```python
from openapi_client.models.process_info import ProcessInfo

# TODO update the JSON string below
json = "{}"
# create an instance of ProcessInfo from a JSON string
process_info_instance = ProcessInfo.from_json(json)
# print the JSON string representation of the object
print(ProcessInfo.to_json())

# convert the object into a dict
process_info_dict = process_info_instance.to_dict()
# create an instance of ProcessInfo from a dict
process_info_from_dict = ProcessInfo.from_dict(process_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


