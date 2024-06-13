# ActivityObject


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | 
**content** | [**ActivityServerEntityContent**](ActivityServerEntityContent.md) |  | 
**var_from** | [**ActivityObjectEntity**](ActivityObjectEntity.md) |  | 
**to** | [**ActivityObjectEntity**](ActivityObjectEntity.md) |  | 

## Example

```python
from openapi_client.models.activity_object import ActivityObject

# TODO update the JSON string below
json = "{}"
# create an instance of ActivityObject from a JSON string
activity_object_instance = ActivityObject.from_json(json)
# print the JSON string representation of the object
print(ActivityObject.to_json())

# convert the object into a dict
activity_object_dict = activity_object_instance.to_dict()
# create an instance of ActivityObject from a dict
activity_object_from_dict = ActivityObject.from_dict(activity_object_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


