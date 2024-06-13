# UpdateBackupRemoteStorageS3


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**region** | **str** |  | [optional] 
**endpoint** | **str** |  | [optional] 
**bucket** | **str** |  | [optional] 
**access_key_id** | **str** |  | [optional] 
**access_key_secret** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.update_backup_remote_storage_s3 import UpdateBackupRemoteStorageS3

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateBackupRemoteStorageS3 from a JSON string
update_backup_remote_storage_s3_instance = UpdateBackupRemoteStorageS3.from_json(json)
# print the JSON string representation of the object
print(UpdateBackupRemoteStorageS3.to_json())

# convert the object into a dict
update_backup_remote_storage_s3_dict = update_backup_remote_storage_s3_instance.to_dict()
# create an instance of UpdateBackupRemoteStorageS3 from a dict
update_backup_remote_storage_s3_from_dict = UpdateBackupRemoteStorageS3.from_dict(update_backup_remote_storage_s3_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


