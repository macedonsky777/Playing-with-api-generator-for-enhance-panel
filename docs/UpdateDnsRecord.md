# UpdateDnsRecord


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**kind** | [**DnsRecordKind**](DnsRecordKind.md) |  | [optional] 
**name** | **str** |  | [optional] 
**value** | **str** |  | [optional] 
**ttl** | **int** | In seconds | [optional] 
**proxy** | **bool** | If CloudFlare enabled, will enable the proxy | [optional] 

## Example

```python
from openapi_client.models.update_dns_record import UpdateDnsRecord

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateDnsRecord from a JSON string
update_dns_record_instance = UpdateDnsRecord.from_json(json)
# print the JSON string representation of the object
print(UpdateDnsRecord.to_json())

# convert the object into a dict
update_dns_record_dict = update_dns_record_instance.to_dict()
# create an instance of UpdateDnsRecord from a dict
update_dns_record_from_dict = UpdateDnsRecord.from_dict(update_dns_record_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


