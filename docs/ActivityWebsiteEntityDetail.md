# ActivityWebsiteEntityDetail


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **str** |  | 
**subscription_id** | **str** |  | [optional] 
**org_id** | **str** |  | 

## Example

```python
from openapi_client.models.activity_website_entity_detail import ActivityWebsiteEntityDetail

# TODO update the JSON string below
json = "{}"
# create an instance of ActivityWebsiteEntityDetail from a JSON string
activity_website_entity_detail_instance = ActivityWebsiteEntityDetail.from_json(json)
# print the JSON string representation of the object
print(ActivityWebsiteEntityDetail.to_json())

# convert the object into a dict
activity_website_entity_detail_dict = activity_website_entity_detail_instance.to_dict()
# create an instance of ActivityWebsiteEntityDetail from a dict
activity_website_entity_detail_from_dict = ActivityWebsiteEntityDetail.from_dict(activity_website_entity_detail_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


