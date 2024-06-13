# UpdateDefaultDnsRecord


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**kind** | [**DnsRecordKind**](DnsRecordKind.md) |  | [optional] 
**name** | **str** |  | [optional] 
**value** | **str** |  | [optional] 
**ttl** | **int** |  | [optional] 
**override_conflicting** | **bool** |  | [optional] [default to False]

## Example

```python
from openapi_client.models.update_default_dns_record import UpdateDefaultDnsRecord

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateDefaultDnsRecord from a JSON string
update_default_dns_record_instance = UpdateDefaultDnsRecord.from_json(json)
# print the JSON string representation of the object
print(UpdateDefaultDnsRecord.to_json())

# convert the object into a dict
update_default_dns_record_dict = update_default_dns_record_instance.to_dict()
# create an instance of UpdateDefaultDnsRecord from a dict
update_default_dns_record_from_dict = UpdateDefaultDnsRecord.from_dict(update_default_dns_record_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


