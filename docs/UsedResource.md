# UsedResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | [**ResourceName**](ResourceName.md) |  | 
**total** | **int** | The total quota of the resource. If not set, the resource has unlimited quota, but the resource usage is still tracked. | [optional] 
**usage** | **int** |  | 

## Example

```python
from openapi_client.models.used_resource import UsedResource

# TODO update the JSON string below
json = "{}"
# create an instance of UsedResource from a JSON string
used_resource_instance = UsedResource.from_json(json)
# print the JSON string representation of the object
print(UsedResource.to_json())

# convert the object into a dict
used_resource_dict = used_resource_instance.to_dict()
# create an instance of UsedResource from a dict
used_resource_from_dict = UsedResource.from_dict(used_resource_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


