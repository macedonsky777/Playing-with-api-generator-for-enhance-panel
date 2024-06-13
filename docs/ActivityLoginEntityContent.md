# ActivityLoginEntityContent


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**detail** | [**ActivityLoginEntityContentDetail**](ActivityLoginEntityContentDetail.md) |  | 

## Example

```python
from openapi_client.models.activity_login_entity_content import ActivityLoginEntityContent

# TODO update the JSON string below
json = "{}"
# create an instance of ActivityLoginEntityContent from a JSON string
activity_login_entity_content_instance = ActivityLoginEntityContent.from_json(json)
# print the JSON string representation of the object
print(ActivityLoginEntityContent.to_json())

# convert the object into a dict
activity_login_entity_content_dict = activity_login_entity_content_instance.to_dict()
# create an instance of ActivityLoginEntityContent from a dict
activity_login_entity_content_from_dict = ActivityLoginEntityContent.from_dict(activity_login_entity_content_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


