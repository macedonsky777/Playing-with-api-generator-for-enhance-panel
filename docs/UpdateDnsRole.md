# UpdateDnsRole


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**state** | [**ServerRoleState**](ServerRoleState.md) |  | [optional] 

## Example

```python
from openapi_client.models.update_dns_role import UpdateDnsRole

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateDnsRole from a JSON string
update_dns_role_instance = UpdateDnsRole.from_json(json)
# print the JSON string representation of the object
print(UpdateDnsRole.to_json())

# convert the object into a dict
update_dns_role_dict = update_dns_role_instance.to_dict()
# create an instance of UpdateDnsRole from a dict
update_dns_role_from_dict = UpdateDnsRole.from_dict(update_dns_role_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


