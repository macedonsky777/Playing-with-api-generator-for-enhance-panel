# ServerStatusUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**is_decommissioned** | **bool** |  | [optional] 

## Example

```python
from openapi_client.models.server_status_update import ServerStatusUpdate

# TODO update the JSON string below
json = "{}"
# create an instance of ServerStatusUpdate from a JSON string
server_status_update_instance = ServerStatusUpdate.from_json(json)
# print the JSON string representation of the object
print(ServerStatusUpdate.to_json())

# convert the object into a dict
server_status_update_dict = server_status_update_instance.to_dict()
# create an instance of ServerStatusUpdate from a dict
server_status_update_from_dict = ServerStatusUpdate.from_dict(server_status_update_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


