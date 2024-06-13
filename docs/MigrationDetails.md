# MigrationDetails


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**website_id** | **str** |  | 
**source_server_id** | **str** |  | 
**dest_server_id** | **str** |  | 
**dest_server_name** | **str** |  | 
**server_role** | [**ServerRole**](ServerRole.md) |  | 
**migration_status** | [**MigrationStatus**](MigrationStatus.md) |  | 
**created_at** | **str** |  | 
**last_updated** | **str** |  | 
**website_primary_domain** | **str** |  | 
**percentage_complete** | **int** |  | 
**session_id** | **str** |  | 

## Example

```python
from openapi_client.models.migration_details import MigrationDetails

# TODO update the JSON string below
json = "{}"
# create an instance of MigrationDetails from a JSON string
migration_details_instance = MigrationDetails.from_json(json)
# print the JSON string representation of the object
print(MigrationDetails.to_json())

# convert the object into a dict
migration_details_dict = migration_details_instance.to_dict()
# create an instance of MigrationDetails from a dict
migration_details_from_dict = MigrationDetails.from_dict(migration_details_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


