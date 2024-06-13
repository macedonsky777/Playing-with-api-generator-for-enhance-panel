# WpUsersFullListing


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[WpUser]**](WpUser.md) |  | 

## Example

```python
from openapi_client.models.wp_users_full_listing import WpUsersFullListing

# TODO update the JSON string below
json = "{}"
# create an instance of WpUsersFullListing from a JSON string
wp_users_full_listing_instance = WpUsersFullListing.from_json(json)
# print the JSON string representation of the object
print(WpUsersFullListing.to_json())

# convert the object into a dict
wp_users_full_listing_dict = wp_users_full_listing_instance.to_dict()
# create an instance of WpUsersFullListing from a dict
wp_users_full_listing_from_dict = WpUsersFullListing.from_dict(wp_users_full_listing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


