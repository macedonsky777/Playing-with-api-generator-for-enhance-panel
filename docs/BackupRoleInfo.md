# BackupRoleInfo


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**state** | [**ServerRoleState**](ServerRoleState.md) |  | 
**usage** | **int** |  | 
**snapshots_count** | **int** |  | 
**last24h_snapshots_count** | **int** |  | 
**bkupd** | [**ServiceInfo**](ServiceInfo.md) |  | 
**websites_count** | **int** | The number of websites whose backups are assigned to be on this backup role. | 

## Example

```python
from openapi_client.models.backup_role_info import BackupRoleInfo

# TODO update the JSON string below
json = "{}"
# create an instance of BackupRoleInfo from a JSON string
backup_role_info_instance = BackupRoleInfo.from_json(json)
# print the JSON string representation of the object
print(BackupRoleInfo.to_json())

# convert the object into a dict
backup_role_info_dict = backup_role_info_instance.to_dict()
# create an instance of BackupRoleInfo from a dict
backup_role_info_from_dict = BackupRoleInfo.from_dict(backup_role_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


