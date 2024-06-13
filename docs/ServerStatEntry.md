# ServerStatEntry

Each entry represts server stats recorded periodically

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**server_id** | **str** |  | 
**io_wait** | **float** |  | 
**ram_usage** | **float** |  | 
**swap_usage** | **float** |  | 
**system_load** | **float** |  | 
**uptime** | **float** |  | 
**recorded_at** | **datetime** | Time when the entry was recorded | 

## Example

```python
from openapi_client.models.server_stat_entry import ServerStatEntry

# TODO update the JSON string below
json = "{}"
# create an instance of ServerStatEntry from a JSON string
server_stat_entry_instance = ServerStatEntry.from_json(json)
# print the JSON string representation of the object
print(ServerStatEntry.to_json())

# convert the object into a dict
server_stat_entry_dict = server_stat_entry_instance.to_dict()
# create an instance of ServerStatEntry from a dict
server_stat_entry_from_dict = ServerStatEntry.from_dict(server_stat_entry_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


