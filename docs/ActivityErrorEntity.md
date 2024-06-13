# ActivityErrorEntity


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | 
**content** | [**ActivityErrorEntityContent**](ActivityErrorEntityContent.md) |  | 

## Example

```python
from openapi_client.models.activity_error_entity import ActivityErrorEntity

# TODO update the JSON string below
json = "{}"
# create an instance of ActivityErrorEntity from a JSON string
activity_error_entity_instance = ActivityErrorEntity.from_json(json)
# print the JSON string representation of the object
print(ActivityErrorEntity.to_json())

# convert the object into a dict
activity_error_entity_dict = activity_error_entity_instance.to_dict()
# create an instance of ActivityErrorEntity from a dict
activity_error_entity_from_dict = ActivityErrorEntity.from_dict(activity_error_entity_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


