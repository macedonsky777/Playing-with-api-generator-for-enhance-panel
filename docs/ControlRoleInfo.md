# ControlRoleInfo


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**usage** | **int** |  | 
**authd** | [**CoreServiceInfo**](CoreServiceInfo.md) |  | 
**sged** | [**CoreServiceInfo**](CoreServiceInfo.md) |  | 
**logd** | [**CoreServiceInfo**](CoreServiceInfo.md) |  | 

## Example

```python
from openapi_client.models.control_role_info import ControlRoleInfo

# TODO update the JSON string below
json = "{}"
# create an instance of ControlRoleInfo from a JSON string
control_role_info_instance = ControlRoleInfo.from_json(json)
# print the JSON string representation of the object
print(ControlRoleInfo.to_json())

# convert the object into a dict
control_role_info_dict = control_role_info_instance.to_dict()
# create an instance of ControlRoleInfo from a dict
control_role_info_from_dict = ControlRoleInfo.from_dict(control_role_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


