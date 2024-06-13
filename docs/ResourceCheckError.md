# ResourceCheckError


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**conflicts** | [**List[ResourceCheckConflict]**](ResourceCheckConflict.md) |  | [optional] 
**resources** | [**List[ResourceCheckManagerError]**](ResourceCheckManagerError.md) |  | [optional] 

## Example

```python
from openapi_client.models.resource_check_error import ResourceCheckError

# TODO update the JSON string below
json = "{}"
# create an instance of ResourceCheckError from a JSON string
resource_check_error_instance = ResourceCheckError.from_json(json)
# print the JSON string representation of the object
print(ResourceCheckError.to_json())

# convert the object into a dict
resource_check_error_dict = resource_check_error_instance.to_dict()
# create an instance of ResourceCheckError from a dict
resource_check_error_from_dict = ResourceCheckError.from_dict(resource_check_error_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


