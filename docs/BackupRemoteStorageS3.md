# BackupRemoteStorageS3


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**purpose** | [**RemoteStoragePurpose**](RemoteStoragePurpose.md) |  | 
**region** | **str** |  | 
**endpoint** | **str** |  | 
**bucket** | **str** |  | 
**access_key_id** | **str** |  | 
**prefix** | **str** |  | 

## Example

```python
from openapi_client.models.backup_remote_storage_s3 import BackupRemoteStorageS3

# TODO update the JSON string below
json = "{}"
# create an instance of BackupRemoteStorageS3 from a JSON string
backup_remote_storage_s3_instance = BackupRemoteStorageS3.from_json(json)
# print the JSON string representation of the object
print(BackupRemoteStorageS3.to_json())

# convert the object into a dict
backup_remote_storage_s3_dict = backup_remote_storage_s3_instance.to_dict()
# create an instance of BackupRemoteStorageS3 from a dict
backup_remote_storage_s3_from_dict = BackupRemoteStorageS3.from_dict(backup_remote_storage_s3_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


