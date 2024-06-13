# ImportMigrationEntry


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**org_id** | **str** |  | 
**filename** | **str** |  | 
**filesize** | **int** |  | 
**status** | **str** |  | 
**import_type** | **str** |  | 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 
**percentage_complete** | **int** |  | 
**primary_domain** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.import_migration_entry import ImportMigrationEntry

# TODO update the JSON string below
json = "{}"
# create an instance of ImportMigrationEntry from a JSON string
import_migration_entry_instance = ImportMigrationEntry.from_json(json)
# print the JSON string representation of the object
print(ImportMigrationEntry.to_json())

# convert the object into a dict
import_migration_entry_dict = import_migration_entry_instance.to_dict()
# create an instance of ImportMigrationEntry from a dict
import_migration_entry_from_dict = ImportMigrationEntry.from_dict(import_migration_entry_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


