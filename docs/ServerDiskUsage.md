# ServerDiskUsage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**disks** | [**List[Disk]**](Disk.md) |  | [optional] 

## Example

```python
from openapi_client.models.server_disk_usage import ServerDiskUsage

# TODO update the JSON string below
json = "{}"
# create an instance of ServerDiskUsage from a JSON string
server_disk_usage_instance = ServerDiskUsage.from_json(json)
# print the JSON string representation of the object
print(ServerDiskUsage.to_json())

# convert the object into a dict
server_disk_usage_dict = server_disk_usage_instance.to_dict()
# create an instance of ServerDiskUsage from a dict
server_disk_usage_from_dict = ServerDiskUsage.from_dict(server_disk_usage_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


