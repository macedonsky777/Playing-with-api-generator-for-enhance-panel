# UpdateDatabaseRole


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**state** | [**ServerRoleState**](ServerRoleState.md) |  | [optional] 

## Example

```python
from openapi_client.models.update_database_role import UpdateDatabaseRole

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateDatabaseRole from a JSON string
update_database_role_instance = UpdateDatabaseRole.from_json(json)
# print the JSON string representation of the object
print(UpdateDatabaseRole.to_json())

# convert the object into a dict
update_database_role_dict = update_database_role_instance.to_dict()
# create an instance of UpdateDatabaseRole from a dict
update_database_role_from_dict = UpdateDatabaseRole.from_dict(update_database_role_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


