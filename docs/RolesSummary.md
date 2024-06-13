# RolesSummary


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | [**RoleSummary**](RoleSummary.md) |  | [optional] 
**backup** | [**RoleSummary**](RoleSummary.md) |  | [optional] 
**database** | [**RoleSummary**](RoleSummary.md) |  | [optional] 
**application** | [**RoleSummary**](RoleSummary.md) |  | [optional] 
**dns** | [**RoleSummary**](RoleSummary.md) |  | [optional] 
**control_panel** | [**RoleSummary**](RoleSummary.md) |  | [optional] 

## Example

```python
from openapi_client.models.roles_summary import RolesSummary

# TODO update the JSON string below
json = "{}"
# create an instance of RolesSummary from a JSON string
roles_summary_instance = RolesSummary.from_json(json)
# print the JSON string representation of the object
print(RolesSummary.to_json())

# convert the object into a dict
roles_summary_dict = roles_summary_instance.to_dict()
# create an instance of RolesSummary from a dict
roles_summary_from_dict = RolesSummary.from_dict(roles_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


