# ImportMigrationLogEntry


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**created_at** | **str** |  | 
**migration_id** | **str** |  | 
**log_data** | **str** |  | 
**percentage_complete** | **int** |  | 
**level** | [**LogLevel**](LogLevel.md) |  | 
**action** | [**LogAction**](LogAction.md) |  | 
**kind** | [**LogKind**](LogKind.md) |  | 

## Example

```python
from openapi_client.models.import_migration_log_entry import ImportMigrationLogEntry

# TODO update the JSON string below
json = "{}"
# create an instance of ImportMigrationLogEntry from a JSON string
import_migration_log_entry_instance = ImportMigrationLogEntry.from_json(json)
# print the JSON string representation of the object
print(ImportMigrationLogEntry.to_json())

# convert the object into a dict
import_migration_log_entry_dict = import_migration_log_entry_instance.to_dict()
# create an instance of ImportMigrationLogEntry from a dict
import_migration_log_entry_from_dict = ImportMigrationLogEntry.from_dict(import_migration_log_entry_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


