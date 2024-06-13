# Backup


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**website_id** | **str** |  | 
**started_at** | **str** |  | 
**finished_at** | **str** |  | [optional] 
**snapshot_dir_name** | **str** |  | 
**size** | **int** |  | [optional] 
**home_dir_status** | [**OperationStatus**](OperationStatus.md) |  | [optional] 
**files_size** | **int** |  | [optional] 
**mysql_dbs_status** | [**OperationStatus**](OperationStatus.md) |  | [optional] 
**mysql_dbs_count** | **int** |  | [optional] 
**mysql_dbs_size** | **int** |  | [optional] 
**emails_status** | [**OperationStatus**](OperationStatus.md) |  | [optional] 
**emails_count** | **int** |  | [optional] 
**emails_size** | **int** |  | [optional] 
**kind** | [**BackupKind**](BackupKind.md) |  | 
**description** | **str** |  | [optional] 
**storage_kind** | [**BackupStorageKind**](BackupStorageKind.md) |  | 

## Example

```python
from openapi_client.models.backup import Backup

# TODO update the JSON string below
json = "{}"
# create an instance of Backup from a JSON string
backup_instance = Backup.from_json(json)
# print the JSON string representation of the object
print(Backup.to_json())

# convert the object into a dict
backup_dict = backup_instance.to_dict()
# create an instance of Backup from a dict
backup_from_dict = Backup.from_dict(backup_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


