# ActivityObjectEntity


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | 
**content** | [**ActivityServerEntityContent**](ActivityServerEntityContent.md) |  | 

## Example

```python
from openapi_client.models.activity_object_entity import ActivityObjectEntity

# TODO update the JSON string below
json = "{}"
# create an instance of ActivityObjectEntity from a JSON string
activity_object_entity_instance = ActivityObjectEntity.from_json(json)
# print the JSON string representation of the object
print(ActivityObjectEntity.to_json())

# convert the object into a dict
activity_object_entity_dict = activity_object_entity_instance.to_dict()
# create an instance of ActivityObjectEntity from a dict
activity_object_entity_from_dict = ActivityObjectEntity.from_dict(activity_object_entity_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


