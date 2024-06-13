# UpdateDnsZone


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name_server** | **str** |  | [optional] 
**admin_email** | **str** |  | [optional] 
**expire** | **int** |  | [optional] 
**refresh** | **int** |  | [optional] 
**retry** | **int** |  | [optional] 
**ttl** | **int** | In seconds | [optional] 

## Example

```python
from openapi_client.models.update_dns_zone import UpdateDnsZone

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateDnsZone from a JSON string
update_dns_zone_instance = UpdateDnsZone.from_json(json)
# print the JSON string representation of the object
print(UpdateDnsZone.to_json())

# convert the object into a dict
update_dns_zone_dict = update_dns_zone_instance.to_dict()
# create an instance of UpdateDnsZone from a dict
update_dns_zone_from_dict = UpdateDnsZone.from_dict(update_dns_zone_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


