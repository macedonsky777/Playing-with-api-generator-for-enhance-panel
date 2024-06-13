# BackupDetailed


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**website_id** | **str** |  | 
**started_at** | **datetime** |  | 
**finished_at** | **datetime** |  | [optional] 
**snapshot_dir_name** | **str** |  | 
**size** | **int** |  | [optional] 
**home_dir_status** | [**OperationStatus**](OperationStatus.md) |  | [optional] 
**files_size** | **int** |  | [optional] 
**mysql_dbs_status** | [**OperationStatus**](OperationStatus.md) |  | [optional] 
**mysql_dbs** | **List[str]** |  | [optional] 
**mysql_dbs_size** | **int** |  | [optional] 
**emails_status** | [**OperationStatus**](OperationStatus.md) |  | [optional] 
**emails** | **List[str]** | The addresses of the backed up mailboxes. | [optional] 
**email_domains** | **List[str]** | The domain ids of the backed up mailboxes. | [optional] 
**emails_size** | **int** |  | [optional] 
**kind** | [**BackupKind**](BackupKind.md) |  | 
**description** | **str** |  | [optional] 
**storage_kind** | [**BackupStorageKind**](BackupStorageKind.md) |  | 

## Example

```python
from openapi_client.models.backup_detailed import BackupDetailed

# TODO update the JSON string below
json = "{}"
# create an instance of BackupDetailed from a JSON string
backup_detailed_instance = BackupDetailed.from_json(json)
# print the JSON string representation of the object
print(BackupDetailed.to_json())

# convert the object into a dict
backup_detailed_dict = backup_detailed_instance.to_dict()
# create an instance of BackupDetailed from a dict
backup_detailed_from_dict = BackupDetailed.from_dict(backup_detailed_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


