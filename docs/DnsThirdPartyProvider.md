# DnsThirdPartyProvider


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**url** | **str** |  | 
**headers** | **Dict[str, str]** | Map of string keys to string values. | [optional] 

## Example

```python
from openapi_client.models.dns_third_party_provider import DnsThirdPartyProvider

# TODO update the JSON string below
json = "{}"
# create an instance of DnsThirdPartyProvider from a JSON string
dns_third_party_provider_instance = DnsThirdPartyProvider.from_json(json)
# print the JSON string representation of the object
print(DnsThirdPartyProvider.to_json())

# convert the object into a dict
dns_third_party_provider_dict = dns_third_party_provider_instance.to_dict()
# create an instance of DnsThirdPartyProvider from a dict
dns_third_party_provider_from_dict = DnsThirdPartyProvider.from_dict(dns_third_party_provider_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


