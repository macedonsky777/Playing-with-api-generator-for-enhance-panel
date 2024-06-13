# DomainSslCert


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cn** | **str** |  | 
**expires** | **str** |  | 
**issued** | **str** |  | 
**issuer** | **str** |  | 
**sans** | **List[str]** |  | 
**force_https** | **bool** |  | 

## Example

```python
from openapi_client.models.domain_ssl_cert import DomainSslCert

# TODO update the JSON string below
json = "{}"
# create an instance of DomainSslCert from a JSON string
domain_ssl_cert_instance = DomainSslCert.from_json(json)
# print the JSON string representation of the object
print(DomainSslCert.to_json())

# convert the object into a dict
domain_ssl_cert_dict = domain_ssl_cert_instance.to_dict()
# create an instance of DomainSslCert from a dict
domain_ssl_cert_from_dict = DomainSslCert.from_dict(domain_ssl_cert_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


