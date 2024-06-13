# ResourceCheckConflict


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**kind** | [**ResourceCheckConflictKind**](ResourceCheckConflictKind.md) |  | 
**id** | **str** |  | 
**name** | **str** |  | 

## Example

```python
from openapi_client.models.resource_check_conflict import ResourceCheckConflict

# TODO update the JSON string below
json = "{}"
# create an instance of ResourceCheckConflict from a JSON string
resource_check_conflict_instance = ResourceCheckConflict.from_json(json)
# print the JSON string representation of the object
print(ResourceCheckConflict.to_json())

# convert the object into a dict
resource_check_conflict_dict = resource_check_conflict_instance.to_dict()
# create an instance of ResourceCheckConflict from a dict
resource_check_conflict_from_dict = ResourceCheckConflict.from_dict(resource_check_conflict_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


