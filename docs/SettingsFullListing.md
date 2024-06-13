# SettingsFullListing


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[Setting]**](Setting.md) |  | 

## Example

```python
from openapi_client.models.settings_full_listing import SettingsFullListing

# TODO update the JSON string below
json = "{}"
# create an instance of SettingsFullListing from a JSON string
settings_full_listing_instance = SettingsFullListing.from_json(json)
# print the JSON string representation of the object
print(SettingsFullListing.to_json())

# convert the object into a dict
settings_full_listing_dict = settings_full_listing_instance.to_dict()
# create an instance of SettingsFullListing from a dict
settings_full_listing_from_dict = SettingsFullListing.from_dict(settings_full_listing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


