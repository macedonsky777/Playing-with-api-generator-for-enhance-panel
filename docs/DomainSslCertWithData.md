# DomainSslCertWithData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cn** | **str** |  | 
**expires** | **str** |  | 
**issued** | **str** |  | 
**issuer** | **str** |  | 
**sans** | **List[str]** |  | 
**cert** | **str** |  | 
**key** | **str** |  | 
**force_https** | **bool** |  | [optional] 

## Example

```python
from openapi_client.models.domain_ssl_cert_with_data import DomainSslCertWithData

# TODO update the JSON string below
json = "{}"
# create an instance of DomainSslCertWithData from a JSON string
domain_ssl_cert_with_data_instance = DomainSslCertWithData.from_json(json)
# print the JSON string representation of the object
print(DomainSslCertWithData.to_json())

# convert the object into a dict
domain_ssl_cert_with_data_dict = domain_ssl_cert_with_data_instance.to_dict()
# create an instance of DomainSslCertWithData from a dict
domain_ssl_cert_with_data_from_dict = DomainSslCertWithData.from_dict(domain_ssl_cert_with_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


