# ActivityDomainEntity


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | 
**content** | [**ActivityDomainEntityContent**](ActivityDomainEntityContent.md) |  | 

## Example

```python
from openapi_client.models.activity_domain_entity import ActivityDomainEntity

# TODO update the JSON string below
json = "{}"
# create an instance of ActivityDomainEntity from a JSON string
activity_domain_entity_instance = ActivityDomainEntity.from_json(json)
# print the JSON string representation of the object
print(ActivityDomainEntity.to_json())

# convert the object into a dict
activity_domain_entity_dict = activity_domain_entity_instance.to_dict()
# create an instance of ActivityDomainEntity from a dict
activity_domain_entity_from_dict = ActivityDomainEntity.from_dict(activity_domain_entity_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


