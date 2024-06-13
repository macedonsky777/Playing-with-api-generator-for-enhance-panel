# ActivityOrgEntityContentDetail


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ok** | [**ActivityOrgEntityDetail**](ActivityOrgEntityDetail.md) |  | [optional] 
**error** | [**HttpError**](HttpError.md) |  | [optional] 

## Example

```python
from openapi_client.models.activity_org_entity_content_detail import ActivityOrgEntityContentDetail

# TODO update the JSON string below
json = "{}"
# create an instance of ActivityOrgEntityContentDetail from a JSON string
activity_org_entity_content_detail_instance = ActivityOrgEntityContentDetail.from_json(json)
# print the JSON string representation of the object
print(ActivityOrgEntityContentDetail.to_json())

# convert the object into a dict
activity_org_entity_content_detail_dict = activity_org_entity_content_detail_instance.to_dict()
# create an instance of ActivityOrgEntityContentDetail from a dict
activity_org_entity_content_detail_from_dict = ActivityOrgEntityContentDetail.from_dict(activity_org_entity_content_detail_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


