# ServerNetworkStats


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**latency** | **float** | Latency to the server in milliseconds. | 
**packet_loss** | **float** | Packet loss percentage | 

## Example

```python
from openapi_client.models.server_network_stats import ServerNetworkStats

# TODO update the JSON string below
json = "{}"
# create an instance of ServerNetworkStats from a JSON string
server_network_stats_instance = ServerNetworkStats.from_json(json)
# print the JSON string representation of the object
print(ServerNetworkStats.to_json())

# convert the object into a dict
server_network_stats_dict = server_network_stats_instance.to_dict()
# create an instance of ServerNetworkStats from a dict
server_network_stats_from_dict = ServerNetworkStats.from_dict(server_network_stats_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


