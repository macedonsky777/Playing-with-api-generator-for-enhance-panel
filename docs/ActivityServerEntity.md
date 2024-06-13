# ActivityServerEntity


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | 
**content** | [**ActivityServerEntityContent**](ActivityServerEntityContent.md) |  | 

## Example

```python
from openapi_client.models.activity_server_entity import ActivityServerEntity

# TODO update the JSON string below
json = "{}"
# create an instance of ActivityServerEntity from a JSON string
activity_server_entity_instance = ActivityServerEntity.from_json(json)
# print the JSON string representation of the object
print(ActivityServerEntity.to_json())

# convert the object into a dict
activity_server_entity_dict = activity_server_entity_instance.to_dict()
# create an instance of ActivityServerEntity from a dict
activity_server_entity_from_dict = ActivityServerEntity.from_dict(activity_server_entity_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


