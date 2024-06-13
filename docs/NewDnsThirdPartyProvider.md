# NewDnsThirdPartyProvider


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** |  | 
**headers** | **Dict[str, str]** | Map of string keys to string values. | [optional] 

## Example

```python
from openapi_client.models.new_dns_third_party_provider import NewDnsThirdPartyProvider

# TODO update the JSON string below
json = "{}"
# create an instance of NewDnsThirdPartyProvider from a JSON string
new_dns_third_party_provider_instance = NewDnsThirdPartyProvider.from_json(json)
# print the JSON string representation of the object
print(NewDnsThirdPartyProvider.to_json())

# convert the object into a dict
new_dns_third_party_provider_dict = new_dns_third_party_provider_instance.to_dict()
# create an instance of NewDnsThirdPartyProvider from a dict
new_dns_third_party_provider_from_dict = NewDnsThirdPartyProvider.from_dict(new_dns_third_party_provider_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


