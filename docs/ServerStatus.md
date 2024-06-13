# ServerStatus


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | [**NetworkStatus**](NetworkStatus.md) |  | 

## Example

```python
from openapi_client.models.server_status import ServerStatus

# TODO update the JSON string below
json = "{}"
# create an instance of ServerStatus from a JSON string
server_status_instance = ServerStatus.from_json(json)
# print the JSON string representation of the object
print(ServerStatus.to_json())

# convert the object into a dict
server_status_dict = server_status_instance.to_dict()
# create an instance of ServerStatus from a dict
server_status_from_dict = ServerStatus.from_dict(server_status_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


