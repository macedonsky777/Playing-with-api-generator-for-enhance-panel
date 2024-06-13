# CreateBackupRemoteStorageS3


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**purpose** | [**RemoteStoragePurpose**](RemoteStoragePurpose.md) |  | 
**region** | **str** |  | 
**endpoint** | **str** |  | 
**bucket** | **str** |  | 
**access_key_id** | **str** |  | 
**access_key_secret** | **str** |  | 
**prefix** | **str** |  | 

## Example

```python
from openapi_client.models.create_backup_remote_storage_s3 import CreateBackupRemoteStorageS3

# TODO update the JSON string below
json = "{}"
# create an instance of CreateBackupRemoteStorageS3 from a JSON string
create_backup_remote_storage_s3_instance = CreateBackupRemoteStorageS3.from_json(json)
# print the JSON string representation of the object
print(CreateBackupRemoteStorageS3.to_json())

# convert the object into a dict
create_backup_remote_storage_s3_dict = create_backup_remote_storage_s3_instance.to_dict()
# create an instance of CreateBackupRemoteStorageS3 from a dict
create_backup_remote_storage_s3_from_dict = CreateBackupRemoteStorageS3.from_dict(create_backup_remote_storage_s3_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


