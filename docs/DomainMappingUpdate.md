# DomainMappingUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**document_root** | **str** |  | [optional] 
**kind** | [**DomainMappingKind**](DomainMappingKind.md) |  | [optional] 

## Example

```python
from openapi_client.models.domain_mapping_update import DomainMappingUpdate

# TODO update the JSON string below
json = "{}"
# create an instance of DomainMappingUpdate from a JSON string
domain_mapping_update_instance = DomainMappingUpdate.from_json(json)
# print the JSON string representation of the object
print(DomainMappingUpdate.to_json())

# convert the object into a dict
domain_mapping_update_dict = domain_mapping_update_instance.to_dict()
# create an instance of DomainMappingUpdate from a dict
domain_mapping_update_from_dict = DomainMappingUpdate.from_dict(domain_mapping_update_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


