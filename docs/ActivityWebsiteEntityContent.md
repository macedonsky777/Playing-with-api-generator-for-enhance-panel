# ActivityWebsiteEntityContent


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**detail** | [**ActivityWebsiteEntityContentDetail**](ActivityWebsiteEntityContentDetail.md) |  | 

## Example

```python
from openapi_client.models.activity_website_entity_content import ActivityWebsiteEntityContent

# TODO update the JSON string below
json = "{}"
# create an instance of ActivityWebsiteEntityContent from a JSON string
activity_website_entity_content_instance = ActivityWebsiteEntityContent.from_json(json)
# print the JSON string representation of the object
print(ActivityWebsiteEntityContent.to_json())

# convert the object into a dict
activity_website_entity_content_dict = activity_website_entity_content_instance.to_dict()
# create an instance of ActivityWebsiteEntityContent from a dict
activity_website_entity_content_from_dict = ActivityWebsiteEntityContent.from_dict(activity_website_entity_content_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


