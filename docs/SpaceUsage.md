# SpaceUsage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total** | **int** |  | 
**used** | **int** |  | 

## Example

```python
from openapi_client.models.space_usage import SpaceUsage

# TODO update the JSON string below
json = "{}"
# create an instance of SpaceUsage from a JSON string
space_usage_instance = SpaceUsage.from_json(json)
# print the JSON string representation of the object
print(SpaceUsage.to_json())

# convert the object into a dict
space_usage_dict = space_usage_instance.to_dict()
# create an instance of SpaceUsage from a dict
space_usage_from_dict = SpaceUsage.from_dict(space_usage_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


