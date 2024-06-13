# ApplicationRoleInfo


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**state** | [**ServerRoleState**](ServerRoleState.md) |  | 
**usage** | **int** |  | 
**filerd** | [**ServiceInfo**](ServiceInfo.md) |  | 
**ftpcd** | [**ServiceInfo**](ServiceInfo.md) |  | 
**websites_count** | **int** | The number of websites that are assigned to be on this application role. | 

## Example

```python
from openapi_client.models.application_role_info import ApplicationRoleInfo

# TODO update the JSON string below
json = "{}"
# create an instance of ApplicationRoleInfo from a JSON string
application_role_info_instance = ApplicationRoleInfo.from_json(json)
# print the JSON string representation of the object
print(ApplicationRoleInfo.to_json())

# convert the object into a dict
application_role_info_dict = application_role_info_instance.to_dict()
# create an instance of ApplicationRoleInfo from a dict
application_role_info_from_dict = ApplicationRoleInfo.from_dict(application_role_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


