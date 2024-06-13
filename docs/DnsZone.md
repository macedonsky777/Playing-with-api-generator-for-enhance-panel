# DnsZone


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**origin** | **str** |  | 
**soa** | [**DnsSoa**](DnsSoa.md) |  | 
**records** | [**List[DnsRecord]**](DnsRecord.md) |  | 
**dnssec_ds_records** | **str** |  | [optional] 
**dnssec_dnskey_records** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.dns_zone import DnsZone

# TODO update the JSON string below
json = "{}"
# create an instance of DnsZone from a JSON string
dns_zone_instance = DnsZone.from_json(json)
# print the JSON string representation of the object
print(DnsZone.to_json())

# convert the object into a dict
dns_zone_dict = dns_zone_instance.to_dict()
# create an instance of DnsZone from a dict
dns_zone_from_dict = DnsZone.from_dict(dns_zone_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


