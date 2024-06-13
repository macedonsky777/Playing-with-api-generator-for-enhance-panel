# ActivityWebsiteEntity


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | 
**content** | [**ActivityWebsiteEntityContent**](ActivityWebsiteEntityContent.md) |  | 

## Example

```python
from openapi_client.models.activity_website_entity import ActivityWebsiteEntity

# TODO update the JSON string below
json = "{}"
# create an instance of ActivityWebsiteEntity from a JSON string
activity_website_entity_instance = ActivityWebsiteEntity.from_json(json)
# print the JSON string representation of the object
print(ActivityWebsiteEntity.to_json())

# convert the object into a dict
activity_website_entity_dict = activity_website_entity_instance.to_dict()
# create an instance of ActivityWebsiteEntity from a dict
activity_website_entity_from_dict = ActivityWebsiteEntity.from_dict(activity_website_entity_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


