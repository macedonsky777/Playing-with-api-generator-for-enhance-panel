# ImporterMigrationReqBody


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subscription_id** | **int** |  | [optional] 
**force_queue** | **bool** |  | [optional] 
**app_server_id** | **str** |  | [optional] 
**backup_server_id** | **str** |  | [optional] 
**db_server_id** | **str** |  | [optional] 
**email_server_id** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.importer_migration_req_body import ImporterMigrationReqBody

# TODO update the JSON string below
json = "{}"
# create an instance of ImporterMigrationReqBody from a JSON string
importer_migration_req_body_instance = ImporterMigrationReqBody.from_json(json)
# print the JSON string representation of the object
print(ImporterMigrationReqBody.to_json())

# convert the object into a dict
importer_migration_req_body_dict = importer_migration_req_body_instance.to_dict()
# create an instance of ImporterMigrationReqBody from a dict
importer_migration_req_body_from_dict = ImporterMigrationReqBody.from_dict(importer_migration_req_body_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


