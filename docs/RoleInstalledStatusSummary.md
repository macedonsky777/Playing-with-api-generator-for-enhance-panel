# RoleInstalledStatusSummary


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**application** | [**RoleInstallationState**](RoleInstallationState.md) |  | [optional] 
**backup** | [**RoleInstallationState**](RoleInstallationState.md) |  | [optional] 
**database** | [**RoleInstallationState**](RoleInstallationState.md) |  | [optional] 
**dns** | [**RoleInstallationState**](RoleInstallationState.md) |  | [optional] 
**email** | [**RoleInstallationState**](RoleInstallationState.md) |  | [optional] 

## Example

```python
from openapi_client.models.role_installed_status_summary import RoleInstalledStatusSummary

# TODO update the JSON string below
json = "{}"
# create an instance of RoleInstalledStatusSummary from a JSON string
role_installed_status_summary_instance = RoleInstalledStatusSummary.from_json(json)
# print the JSON string representation of the object
print(RoleInstalledStatusSummary.to_json())

# convert the object into a dict
role_installed_status_summary_dict = role_installed_status_summary_instance.to_dict()
# create an instance of RoleInstalledStatusSummary from a dict
role_installed_status_summary_from_dict = RoleInstalledStatusSummary.from_dict(role_installed_status_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


