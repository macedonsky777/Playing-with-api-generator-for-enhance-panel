# ActivityLoginEntity


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | 
**content** | [**ActivityLoginEntityContent**](ActivityLoginEntityContent.md) |  | 

## Example

```python
from openapi_client.models.activity_login_entity import ActivityLoginEntity

# TODO update the JSON string below
json = "{}"
# create an instance of ActivityLoginEntity from a JSON string
activity_login_entity_instance = ActivityLoginEntity.from_json(json)
# print the JSON string representation of the object
print(ActivityLoginEntity.to_json())

# convert the object into a dict
activity_login_entity_dict = activity_login_entity_instance.to_dict()
# create an instance of ActivityLoginEntity from a dict
activity_login_entity_from_dict = ActivityLoginEntity.from_dict(activity_login_entity_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


