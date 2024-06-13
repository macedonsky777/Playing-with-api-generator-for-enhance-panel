# BackupRestoreOptions


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**restore_files** | **bool** | If set to false, the backup restoration will not include the website home directory. | [optional] [default to True]
**restore_emails** | **bool** | If set to false, the backup restoration will not include the website emails. | [optional] [default to False]
**restore_databases** | **List[str]** | The list of databases names that need to be restored. If this list is not specified all the databases found in the backup snapshot will be restored, otherwise if this list is specified as empty, no database will be restored. | [optional] 

## Example

```python
from openapi_client.models.backup_restore_options import BackupRestoreOptions

# TODO update the JSON string below
json = "{}"
# create an instance of BackupRestoreOptions from a JSON string
backup_restore_options_instance = BackupRestoreOptions.from_json(json)
# print the JSON string representation of the object
print(BackupRestoreOptions.to_json())

# convert the object into a dict
backup_restore_options_dict = backup_restore_options_instance.to_dict()
# create an instance of BackupRestoreOptions from a dict
backup_restore_options_from_dict = BackupRestoreOptions.from_dict(backup_restore_options_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


