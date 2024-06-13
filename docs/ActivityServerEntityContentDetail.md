# ActivityServerEntityContentDetail


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ok** | [**ActivityServerEntityDetail**](ActivityServerEntityDetail.md) |  | [optional] 
**error** | [**HttpError**](HttpError.md) |  | [optional] 

## Example

```python
from openapi_client.models.activity_server_entity_content_detail import ActivityServerEntityContentDetail

# TODO update the JSON string below
json = "{}"
# create an instance of ActivityServerEntityContentDetail from a JSON string
activity_server_entity_content_detail_instance = ActivityServerEntityContentDetail.from_json(json)
# print the JSON string representation of the object
print(ActivityServerEntityContentDetail.to_json())

# convert the object into a dict
activity_server_entity_content_detail_dict = activity_server_entity_content_detail_instance.to_dict()
# create an instance of ActivityServerEntityContentDetail from a dict
activity_server_entity_content_detail_from_dict = ActivityServerEntityContentDetail.from_dict(activity_server_entity_content_detail_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


