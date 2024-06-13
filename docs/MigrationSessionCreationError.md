# MigrationSessionCreationError


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**migrations** | [**List[MigrationCreationOutcome]**](MigrationCreationOutcome.md) |  | 

## Example

```python
from openapi_client.models.migration_session_creation_error import MigrationSessionCreationError

# TODO update the JSON string below
json = "{}"
# create an instance of MigrationSessionCreationError from a JSON string
migration_session_creation_error_instance = MigrationSessionCreationError.from_json(json)
# print the JSON string representation of the object
print(MigrationSessionCreationError.to_json())

# convert the object into a dict
migration_session_creation_error_dict = migration_session_creation_error_instance.to_dict()
# create an instance of MigrationSessionCreationError from a dict
migration_session_creation_error_from_dict = MigrationSessionCreationError.from_dict(migration_session_creation_error_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


