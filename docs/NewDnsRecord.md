# NewDnsRecord


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**kind** | [**DnsRecordKind**](DnsRecordKind.md) |  | 
**name** | **str** |  | 
**value** | **str** |  | 
**ttl** | **int** |  | [optional] 
**proxy** | **bool** |  | [optional] 

## Example

```python
from openapi_client.models.new_dns_record import NewDnsRecord

# TODO update the JSON string below
json = "{}"
# create an instance of NewDnsRecord from a JSON string
new_dns_record_instance = NewDnsRecord.from_json(json)
# print the JSON string representation of the object
print(NewDnsRecord.to_json())

# convert the object into a dict
new_dns_record_dict = new_dns_record_instance.to_dict()
# create an instance of NewDnsRecord from a dict
new_dns_record_from_dict = NewDnsRecord.from_dict(new_dns_record_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


