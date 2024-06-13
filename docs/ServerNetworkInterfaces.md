# ServerNetworkInterfaces


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**interfaces** | [**List[NetworkInterface]**](NetworkInterface.md) |  | [optional] 

## Example

```python
from openapi_client.models.server_network_interfaces import ServerNetworkInterfaces

# TODO update the JSON string below
json = "{}"
# create an instance of ServerNetworkInterfaces from a JSON string
server_network_interfaces_instance = ServerNetworkInterfaces.from_json(json)
# print the JSON string representation of the object
print(ServerNetworkInterfaces.to_json())

# convert the object into a dict
server_network_interfaces_dict = server_network_interfaces_instance.to_dict()
# create an instance of ServerNetworkInterfaces from a dict
server_network_interfaces_from_dict = ServerNetworkInterfaces.from_dict(server_network_interfaces_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


