# UpdateApplicationRole


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**state** | [**ServerRoleState**](ServerRoleState.md) |  | [optional] 

## Example

```python
from openapi_client.models.update_application_role import UpdateApplicationRole

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateApplicationRole from a JSON string
update_application_role_instance = UpdateApplicationRole.from_json(json)
# print the JSON string representation of the object
print(UpdateApplicationRole.to_json())

# convert the object into a dict
update_application_role_dict = update_application_role_instance.to_dict()
# create an instance of UpdateApplicationRole from a dict
update_application_role_from_dict = UpdateApplicationRole.from_dict(update_application_role_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


