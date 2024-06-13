# MigrationSessionsListing


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[MigrationSessionDetails]**](MigrationSessionDetails.md) |  | 
**total** | **int** |  | 

## Example

```python
from openapi_client.models.migration_sessions_listing import MigrationSessionsListing

# TODO update the JSON string below
json = "{}"
# create an instance of MigrationSessionsListing from a JSON string
migration_sessions_listing_instance = MigrationSessionsListing.from_json(json)
# print the JSON string representation of the object
print(MigrationSessionsListing.to_json())

# convert the object into a dict
migration_sessions_listing_dict = migration_sessions_listing_instance.to_dict()
# create an instance of MigrationSessionsListing from a dict
migration_sessions_listing_from_dict = MigrationSessionsListing.from_dict(migration_sessions_listing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


