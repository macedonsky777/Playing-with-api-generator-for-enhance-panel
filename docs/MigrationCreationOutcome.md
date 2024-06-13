# MigrationCreationOutcome

error and migrationId are mutually exclusive

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | [**HttpError**](HttpError.md) |  | [optional] 
**migration_id** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.migration_creation_outcome import MigrationCreationOutcome

# TODO update the JSON string below
json = "{}"
# create an instance of MigrationCreationOutcome from a JSON string
migration_creation_outcome_instance = MigrationCreationOutcome.from_json(json)
# print the JSON string representation of the object
print(MigrationCreationOutcome.to_json())

# convert the object into a dict
migration_creation_outcome_dict = migration_creation_outcome_instance.to_dict()
# create an instance of MigrationCreationOutcome from a dict
migration_creation_outcome_from_dict = MigrationCreationOutcome.from_dict(migration_creation_outcome_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


