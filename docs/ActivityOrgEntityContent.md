# ActivityOrgEntityContent


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**detail** | [**ActivityOrgEntityContentDetail**](ActivityOrgEntityContentDetail.md) |  | 

## Example

```python
from openapi_client.models.activity_org_entity_content import ActivityOrgEntityContent

# TODO update the JSON string below
json = "{}"
# create an instance of ActivityOrgEntityContent from a JSON string
activity_org_entity_content_instance = ActivityOrgEntityContent.from_json(json)
# print the JSON string representation of the object
print(ActivityOrgEntityContent.to_json())

# convert the object into a dict
activity_org_entity_content_dict = activity_org_entity_content_instance.to_dict()
# create an instance of ActivityOrgEntityContent from a dict
activity_org_entity_content_from_dict = ActivityOrgEntityContent.from_dict(activity_org_entity_content_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


