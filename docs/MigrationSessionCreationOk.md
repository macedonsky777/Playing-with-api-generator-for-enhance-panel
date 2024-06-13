# MigrationSessionCreationOk


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**session_id** | **str** |  | 
**ok_count** | **int** |  | 
**migrations** | [**List[MigrationCreationOutcome]**](MigrationCreationOutcome.md) |  | 

## Example

```python
from openapi_client.models.migration_session_creation_ok import MigrationSessionCreationOk

# TODO update the JSON string below
json = "{}"
# create an instance of MigrationSessionCreationOk from a JSON string
migration_session_creation_ok_instance = MigrationSessionCreationOk.from_json(json)
# print the JSON string representation of the object
print(MigrationSessionCreationOk.to_json())

# convert the object into a dict
migration_session_creation_ok_dict = migration_session_creation_ok_instance.to_dict()
# create an instance of MigrationSessionCreationOk from a dict
migration_session_creation_ok_from_dict = MigrationSessionCreationOk.from_dict(migration_session_creation_ok_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


