# ServerMemoryUsage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ram** | [**SpaceUsage**](SpaceUsage.md) |  | 
**swap** | [**SpaceUsage**](SpaceUsage.md) |  | 

## Example

```python
from openapi_client.models.server_memory_usage import ServerMemoryUsage

# TODO update the JSON string below
json = "{}"
# create an instance of ServerMemoryUsage from a JSON string
server_memory_usage_instance = ServerMemoryUsage.from_json(json)
# print the JSON string representation of the object
print(ServerMemoryUsage.to_json())

# convert the object into a dict
server_memory_usage_dict = server_memory_usage_instance.to_dict()
# create an instance of ServerMemoryUsage from a dict
server_memory_usage_from_dict = ServerMemoryUsage.from_dict(server_memory_usage_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


