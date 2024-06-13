# FtpUsersFullListing


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[FtpUser]**](FtpUser.md) |  | 

## Example

```python
from openapi_client.models.ftp_users_full_listing import FtpUsersFullListing

# TODO update the JSON string below
json = "{}"
# create an instance of FtpUsersFullListing from a JSON string
ftp_users_full_listing_instance = FtpUsersFullListing.from_json(json)
# print the JSON string representation of the object
print(FtpUsersFullListing.to_json())

# convert the object into a dict
ftp_users_full_listing_dict = ftp_users_full_listing_instance.to_dict()
# create an instance of FtpUsersFullListing from a dict
ftp_users_full_listing_from_dict = FtpUsersFullListing.from_dict(ftp_users_full_listing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


