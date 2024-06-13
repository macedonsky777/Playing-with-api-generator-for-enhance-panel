# ImportServerSettingsFullListing


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[ImportServerSettings]**](ImportServerSettings.md) |  | 

## Example

```python
from openapi_client.models.import_server_settings_full_listing import ImportServerSettingsFullListing

# TODO update the JSON string below
json = "{}"
# create an instance of ImportServerSettingsFullListing from a JSON string
import_server_settings_full_listing_instance = ImportServerSettingsFullListing.from_json(json)
# print the JSON string representation of the object
print(ImportServerSettingsFullListing.to_json())

# convert the object into a dict
import_server_settings_full_listing_dict = import_server_settings_full_listing_instance.to_dict()
# create an instance of ImportServerSettingsFullListing from a dict
import_server_settings_full_listing_from_dict = ImportServerSettingsFullListing.from_dict(import_server_settings_full_listing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


