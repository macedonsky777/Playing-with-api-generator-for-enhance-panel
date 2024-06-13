# NewMappedDomain


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **str** |  | 
**document_root** | **str** |  | [optional] 
**kind** | [**DomainMappingKind**](DomainMappingKind.md) |  | [optional] 

## Example

```python
from openapi_client.models.new_mapped_domain import NewMappedDomain

# TODO update the JSON string below
json = "{}"
# create an instance of NewMappedDomain from a JSON string
new_mapped_domain_instance = NewMappedDomain.from_json(json)
# print the JSON string representation of the object
print(NewMappedDomain.to_json())

# convert the object into a dict
new_mapped_domain_dict = new_mapped_domain_instance.to_dict()
# create an instance of NewMappedDomain from a dict
new_mapped_domain_from_dict = NewMappedDomain.from_dict(new_mapped_domain_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


