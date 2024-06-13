# ActivityLoginEntityContentDetail


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ok** | [**ActivityLoginEntityDetail**](ActivityLoginEntityDetail.md) |  | [optional] 
**error** | [**HttpError**](HttpError.md) |  | [optional] 

## Example

```python
from openapi_client.models.activity_login_entity_content_detail import ActivityLoginEntityContentDetail

# TODO update the JSON string below
json = "{}"
# create an instance of ActivityLoginEntityContentDetail from a JSON string
activity_login_entity_content_detail_instance = ActivityLoginEntityContentDetail.from_json(json)
# print the JSON string representation of the object
print(ActivityLoginEntityContentDetail.to_json())

# convert the object into a dict
activity_login_entity_content_detail_dict = activity_login_entity_content_detail_instance.to_dict()
# create an instance of ActivityLoginEntityContentDetail from a dict
activity_login_entity_content_detail_from_dict = ActivityLoginEntityContentDetail.from_dict(activity_login_entity_content_detail_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


