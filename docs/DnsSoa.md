# DnsSoa


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**admin_email** | **str** |  | 
**name_server** | **str** |  | 
**expire** | **int** |  | 
**refresh** | **int** |  | 
**retry** | **int** |  | 
**ttl** | **int** | In seconds | 

## Example

```python
from openapi_client.models.dns_soa import DnsSoa

# TODO update the JSON string below
json = "{}"
# create an instance of DnsSoa from a JSON string
dns_soa_instance = DnsSoa.from_json(json)
# print the JSON string representation of the object
print(DnsSoa.to_json())

# convert the object into a dict
dns_soa_dict = dns_soa_instance.to_dict()
# create an instance of DnsSoa from a dict
dns_soa_from_dict = DnsSoa.from_dict(dns_soa_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


