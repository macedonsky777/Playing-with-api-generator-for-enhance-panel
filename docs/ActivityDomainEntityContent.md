# ActivityDomainEntityContent


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**detail** | [**ActivityDomainEntityContentDetail**](ActivityDomainEntityContentDetail.md) |  | 

## Example

```python
from openapi_client.models.activity_domain_entity_content import ActivityDomainEntityContent

# TODO update the JSON string below
json = "{}"
# create an instance of ActivityDomainEntityContent from a JSON string
activity_domain_entity_content_instance = ActivityDomainEntityContent.from_json(json)
# print the JSON string representation of the object
print(ActivityDomainEntityContent.to_json())

# convert the object into a dict
activity_domain_entity_content_dict = activity_domain_entity_content_instance.to_dict()
# create an instance of ActivityDomainEntityContent from a dict
activity_domain_entity_content_from_dict = ActivityDomainEntityContent.from_dict(activity_domain_entity_content_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


