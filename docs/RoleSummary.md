# RoleSummary


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**state** | [**RoleState**](RoleState.md) |  | 
**status** | [**NetworkStatus**](NetworkStatus.md) |  | [optional] 

## Example

```python
from openapi_client.models.role_summary import RoleSummary

# TODO update the JSON string below
json = "{}"
# create an instance of RoleSummary from a JSON string
role_summary_instance = RoleSummary.from_json(json)
# print the JSON string representation of the object
print(RoleSummary.to_json())

# convert the object into a dict
role_summary_dict = role_summary_instance.to_dict()
# create an instance of RoleSummary from a dict
role_summary_from_dict = RoleSummary.from_dict(role_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


