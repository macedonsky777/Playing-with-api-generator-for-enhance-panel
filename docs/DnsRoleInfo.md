# DnsRoleInfo


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**state** | [**ServerRoleState**](ServerRoleState.md) |  | 
**usage** | **int** |  | 
**zones_count** | **int** |  | 
**dnscd** | [**ServiceInfo**](ServiceInfo.md) |  | 
**websites_count** | **int** | The number of websites whose DNS zones are assigned to be on this dns role. | 

## Example

```python
from openapi_client.models.dns_role_info import DnsRoleInfo

# TODO update the JSON string below
json = "{}"
# create an instance of DnsRoleInfo from a JSON string
dns_role_info_instance = DnsRoleInfo.from_json(json)
# print the JSON string representation of the object
print(DnsRoleInfo.to_json())

# convert the object into a dict
dns_role_info_dict = dns_role_info_instance.to_dict()
# create an instance of DnsRoleInfo from a dict
dns_role_info_from_dict = DnsRoleInfo.from_dict(dns_role_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


