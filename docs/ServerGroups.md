# ServerGroups


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[ServerGroup]**](ServerGroup.md) |  | [optional] 

## Example

```python
from openapi_client.models.server_groups import ServerGroups

# TODO update the JSON string below
json = "{}"
# create an instance of ServerGroups from a JSON string
server_groups_instance = ServerGroups.from_json(json)
# print the JSON string representation of the object
print(ServerGroups.to_json())

# convert the object into a dict
server_groups_dict = server_groups_instance.to_dict()
# create an instance of ServerGroups from a dict
server_groups_from_dict = ServerGroups.from_dict(server_groups_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


