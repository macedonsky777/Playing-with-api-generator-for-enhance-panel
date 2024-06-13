# UpdateServerRoleRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**state** | [**ServerRoleState**](ServerRoleState.md) |  | [optional] 

## Example

```python
from openapi_client.models.update_server_role_request import UpdateServerRoleRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateServerRoleRequest from a JSON string
update_server_role_request_instance = UpdateServerRoleRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateServerRoleRequest.to_json())

# convert the object into a dict
update_server_role_request_dict = update_server_role_request_instance.to_dict()
# create an instance of UpdateServerRoleRequest from a dict
update_server_role_request_from_dict = UpdateServerRoleRequest.from_dict(update_server_role_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


