# MigrationLog


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**created_at** | **str** |  | 
**migration_id** | **str** |  | 
**log_data** | **str** |  | 

## Example

```python
from openapi_client.models.migration_log import MigrationLog

# TODO update the JSON string below
json = "{}"
# create an instance of MigrationLog from a JSON string
migration_log_instance = MigrationLog.from_json(json)
# print the JSON string representation of the object
print(MigrationLog.to_json())

# convert the object into a dict
migration_log_dict = migration_log_instance.to_dict()
# create an instance of MigrationLog from a dict
migration_log_from_dict = MigrationLog.from_dict(migration_log_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


