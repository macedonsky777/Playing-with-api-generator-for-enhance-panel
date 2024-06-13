# BackupStatus


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**website_id** | **str** |  | 
**started_at** | **str** |  | 
**action** | [**BackupAction**](BackupAction.md) |  | 
**home_dir_status** | [**OperationStatus**](OperationStatus.md) |  | [optional] 
**mysql_dbs_status** | [**OperationStatus**](OperationStatus.md) |  | [optional] 
**emails_status** | [**OperationStatus**](OperationStatus.md) |  | [optional] 

## Example

```python
from openapi_client.models.backup_status import BackupStatus

# TODO update the JSON string below
json = "{}"
# create an instance of BackupStatus from a JSON string
backup_status_instance = BackupStatus.from_json(json)
# print the JSON string representation of the object
print(BackupStatus.to_json())

# convert the object into a dict
backup_status_dict = backup_status_instance.to_dict()
# create an instance of BackupStatus from a dict
backup_status_from_dict = BackupStatus.from_dict(backup_status_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


