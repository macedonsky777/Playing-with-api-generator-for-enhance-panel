# RolesInfo


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | [**EmailRoleInfo**](EmailRoleInfo.md) |  | [optional] 
**backup** | [**BackupRoleInfo**](BackupRoleInfo.md) |  | [optional] 
**database** | [**DatabaseRoleInfo**](DatabaseRoleInfo.md) |  | [optional] 
**application** | [**ApplicationRoleInfo**](ApplicationRoleInfo.md) |  | [optional] 
**dns** | [**DnsRoleInfo**](DnsRoleInfo.md) |  | [optional] 
**webserver_kind** | [**WebserverKind**](WebserverKind.md) |  | [optional] 

## Example

```python
from openapi_client.models.roles_info import RolesInfo

# TODO update the JSON string below
json = "{}"
# create an instance of RolesInfo from a JSON string
roles_info_instance = RolesInfo.from_json(json)
# print the JSON string representation of the object
print(RolesInfo.to_json())

# convert the object into a dict
roles_info_dict = roles_info_instance.to_dict()
# create an instance of RolesInfo from a dict
roles_info_from_dict = RolesInfo.from_dict(roles_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


