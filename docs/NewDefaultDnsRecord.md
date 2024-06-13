# NewDefaultDnsRecord


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**kind** | [**DnsRecordKind**](DnsRecordKind.md) |  | 
**name** | **str** |  | 
**value** | **str** |  | 
**ttl** | **int** |  | [optional] 
**override_conflicting** | **bool** |  | [optional] [default to False]

## Example

```python
from openapi_client.models.new_default_dns_record import NewDefaultDnsRecord

# TODO update the JSON string below
json = "{}"
# create an instance of NewDefaultDnsRecord from a JSON string
new_default_dns_record_instance = NewDefaultDnsRecord.from_json(json)
# print the JSON string representation of the object
print(NewDefaultDnsRecord.to_json())

# convert the object into a dict
new_default_dns_record_dict = new_default_dns_record_instance.to_dict()
# create an instance of NewDefaultDnsRecord from a dict
new_default_dns_record_from_dict = NewDefaultDnsRecord.from_dict(new_default_dns_record_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


