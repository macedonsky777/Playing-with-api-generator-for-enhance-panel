# NewPrimaryDomainMapping


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain_id** | **str** |  | 
**canonical_redirect** | [**CanonicalRedirect**](CanonicalRedirect.md) |  | [optional] 

## Example

```python
from openapi_client.models.new_primary_domain_mapping import NewPrimaryDomainMapping

# TODO update the JSON string below
json = "{}"
# create an instance of NewPrimaryDomainMapping from a JSON string
new_primary_domain_mapping_instance = NewPrimaryDomainMapping.from_json(json)
# print the JSON string representation of the object
print(NewPrimaryDomainMapping.to_json())

# convert the object into a dict
new_primary_domain_mapping_dict = new_primary_domain_mapping_instance.to_dict()
# create an instance of NewPrimaryDomainMapping from a dict
new_primary_domain_mapping_from_dict = NewPrimaryDomainMapping.from_dict(new_primary_domain_mapping_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


