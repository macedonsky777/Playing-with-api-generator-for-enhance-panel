# MigrationSessionDetails


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**created_by** | **str** |  | 
**created_at** | **str** |  | 
**updated_at** | **str** |  | 
**migrations_count** | **int** |  | 
**percentage_complete** | **float** |  | 
**not_ready_count** | **int** |  | 

## Example

```python
from openapi_client.models.migration_session_details import MigrationSessionDetails

# TODO update the JSON string below
json = "{}"
# create an instance of MigrationSessionDetails from a JSON string
migration_session_details_instance = MigrationSessionDetails.from_json(json)
# print the JSON string representation of the object
print(MigrationSessionDetails.to_json())

# convert the object into a dict
migration_session_details_dict = migration_session_details_instance.to_dict()
# create an instance of MigrationSessionDetails from a dict
migration_session_details_from_dict = MigrationSessionDetails.from_dict(migration_session_details_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


