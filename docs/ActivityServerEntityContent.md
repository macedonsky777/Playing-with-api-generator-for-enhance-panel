# ActivityServerEntityContent


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**detail** | [**ActivityServerEntityContentDetail**](ActivityServerEntityContentDetail.md) |  | 

## Example

```python
from openapi_client.models.activity_server_entity_content import ActivityServerEntityContent

# TODO update the JSON string below
json = "{}"
# create an instance of ActivityServerEntityContent from a JSON string
activity_server_entity_content_instance = ActivityServerEntityContent.from_json(json)
# print the JSON string representation of the object
print(ActivityServerEntityContent.to_json())

# convert the object into a dict
activity_server_entity_content_dict = activity_server_entity_content_instance.to_dict()
# create an instance of ActivityServerEntityContent from a dict
activity_server_entity_content_from_dict = ActivityServerEntityContent.from_dict(activity_server_entity_content_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


