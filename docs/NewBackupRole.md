# NewBackupRole

The btrfs related information such as mount point and block device paths.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**device_type** | [**DeviceKind**](DeviceKind.md) |  | 
**device_path** | **str** | The full path of the block device. | 
**mount_point** | **str** | The full path where the btrfs will be mounted. | 
**device_size** | **int** | The size of the new device if created as a new sparse file. | [optional] 

## Example

```python
from openapi_client.models.new_backup_role import NewBackupRole

# TODO update the JSON string below
json = "{}"
# create an instance of NewBackupRole from a JSON string
new_backup_role_instance = NewBackupRole.from_json(json)
# print the JSON string representation of the object
print(NewBackupRole.to_json())

# convert the object into a dict
new_backup_role_dict = new_backup_role_instance.to_dict()
# create an instance of NewBackupRole from a dict
new_backup_role_from_dict = NewBackupRole.from_dict(new_backup_role_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


