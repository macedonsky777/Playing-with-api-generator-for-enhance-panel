# ActivityOrgEntity


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | 
**content** | [**ActivityOrgEntityContent**](ActivityOrgEntityContent.md) |  | 

## Example

```python
from openapi_client.models.activity_org_entity import ActivityOrgEntity

# TODO update the JSON string below
json = "{}"
# create an instance of ActivityOrgEntity from a JSON string
activity_org_entity_instance = ActivityOrgEntity.from_json(json)
# print the JSON string representation of the object
print(ActivityOrgEntity.to_json())

# convert the object into a dict
activity_org_entity_dict = activity_org_entity_instance.to_dict()
# create an instance of ActivityOrgEntity from a dict
activity_org_entity_from_dict = ActivityOrgEntity.from_dict(activity_org_entity_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


