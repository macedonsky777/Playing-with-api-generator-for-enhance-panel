# BackupsFullListing


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[Backup]**](Backup.md) |  | 

## Example

```python
from openapi_client.models.backups_full_listing import BackupsFullListing

# TODO update the JSON string below
json = "{}"
# create an instance of BackupsFullListing from a JSON string
backups_full_listing_instance = BackupsFullListing.from_json(json)
# print the JSON string representation of the object
print(BackupsFullListing.to_json())

# convert the object into a dict
backups_full_listing_dict = backups_full_listing_instance.to_dict()
# create an instance of BackupsFullListing from a dict
backups_full_listing_from_dict = BackupsFullListing.from_dict(backups_full_listing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


