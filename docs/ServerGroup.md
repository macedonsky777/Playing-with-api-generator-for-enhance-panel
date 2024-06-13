# ServerGroup


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**name** | **str** |  | 
**server_count** | **float** |  | 
**created_at** | **str** |  | 

## Example

```python
from openapi_client.models.server_group import ServerGroup

# TODO update the JSON string below
json = "{}"
# create an instance of ServerGroup from a JSON string
server_group_instance = ServerGroup.from_json(json)
# print the JSON string representation of the object
print(ServerGroup.to_json())

# convert the object into a dict
server_group_dict = server_group_instance.to_dict()
# create an instance of ServerGroup from a dict
server_group_from_dict = ServerGroup.from_dict(server_group_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


