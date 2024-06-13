# ActivityObjectOneOf


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | 
**var_from** | [**ActivityObjectEntity**](ActivityObjectEntity.md) |  | 
**to** | [**ActivityObjectEntity**](ActivityObjectEntity.md) |  | 

## Example

```python
from openapi_client.models.activity_object_one_of import ActivityObjectOneOf

# TODO update the JSON string below
json = "{}"
# create an instance of ActivityObjectOneOf from a JSON string
activity_object_one_of_instance = ActivityObjectOneOf.from_json(json)
# print the JSON string representation of the object
print(ActivityObjectOneOf.to_json())

# convert the object into a dict
activity_object_one_of_dict = activity_object_one_of_instance.to_dict()
# create an instance of ActivityObjectOneOf from a dict
activity_object_one_of_from_dict = ActivityObjectOneOf.from_dict(activity_object_one_of_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


