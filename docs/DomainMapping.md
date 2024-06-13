# DomainMapping


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain_id** | **str** |  | 
**website_id** | **str** |  | 
**domain** | **str** |  | 
**mapping_kind** | [**DomainMappingKind**](DomainMappingKind.md) |  | 
**document_root** | **str** |  | 
**cert** | [**DomainSslCert**](DomainSslCert.md) |  | [optional] 
**cloudflare_status** | [**CloudFlareStatus**](CloudFlareStatus.md) |  | 
**cloudflare_friendly_name** | **str** |  | [optional] 
**cloudflare_token_id** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.domain_mapping import DomainMapping

# TODO update the JSON string below
json = "{}"
# create an instance of DomainMapping from a JSON string
domain_mapping_instance = DomainMapping.from_json(json)
# print the JSON string representation of the object
print(DomainMapping.to_json())

# convert the object into a dict
domain_mapping_dict = domain_mapping_instance.to_dict()
# create an instance of DomainMapping from a dict
domain_mapping_from_dict = DomainMapping.from_dict(domain_mapping_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


