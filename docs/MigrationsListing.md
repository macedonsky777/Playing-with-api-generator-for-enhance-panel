# MigrationsListing


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[MigrationDetails]**](MigrationDetails.md) |  | 
**total** | **int** |  | 

## Example

```python
from openapi_client.models.migrations_listing import MigrationsListing

# TODO update the JSON string below
json = "{}"
# create an instance of MigrationsListing from a JSON string
migrations_listing_instance = MigrationsListing.from_json(json)
# print the JSON string representation of the object
print(MigrationsListing.to_json())

# convert the object into a dict
migrations_listing_dict = migrations_listing_instance.to_dict()
# create an instance of MigrationsListing from a dict
migrations_listing_from_dict = MigrationsListing.from_dict(migrations_listing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


