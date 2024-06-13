# ResourceCheckManagerError


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**kind** | [**ResourceCheckManagerErrorKind**](ResourceCheckManagerErrorKind.md) |  | 
**resource_name** | [**ResourceName**](ResourceName.md) |  | 
**total** | **int** |  | 
**usage** | **int** |  | 
**requested** | **int** |  | 

## Example

```python
from openapi_client.models.resource_check_manager_error import ResourceCheckManagerError

# TODO update the JSON string below
json = "{}"
# create an instance of ResourceCheckManagerError from a JSON string
resource_check_manager_error_instance = ResourceCheckManagerError.from_json(json)
# print the JSON string representation of the object
print(ResourceCheckManagerError.to_json())

# convert the object into a dict
resource_check_manager_error_dict = resource_check_manager_error_instance.to_dict()
# create an instance of ResourceCheckManagerError from a dict
resource_check_manager_error_from_dict = ResourceCheckManagerError.from_dict(resource_check_manager_error_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


