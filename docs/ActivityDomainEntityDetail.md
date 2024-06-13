# ActivityDomainEntityDetail


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**org_id** | **str** |  | 
**website_id** | **str** |  | [optional] 
**mapping_kind** | [**DomainMappingKind**](DomainMappingKind.md) |  | [optional] 

## Example

```python
from openapi_client.models.activity_domain_entity_detail import ActivityDomainEntityDetail

# TODO update the JSON string below
json = "{}"
# create an instance of ActivityDomainEntityDetail from a JSON string
activity_domain_entity_detail_instance = ActivityDomainEntityDetail.from_json(json)
# print the JSON string representation of the object
print(ActivityDomainEntityDetail.to_json())

# convert the object into a dict
activity_domain_entity_detail_dict = activity_domain_entity_detail_instance.to_dict()
# create an instance of ActivityDomainEntityDetail from a dict
activity_domain_entity_detail_from_dict = ActivityDomainEntityDetail.from_dict(activity_domain_entity_detail_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


