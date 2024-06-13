# SshKeyFullListing


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[SshKey]**](SshKey.md) |  | 

## Example

```python
from openapi_client.models.ssh_key_full_listing import SshKeyFullListing

# TODO update the JSON string below
json = "{}"
# create an instance of SshKeyFullListing from a JSON string
ssh_key_full_listing_instance = SshKeyFullListing.from_json(json)
# print the JSON string representation of the object
print(SshKeyFullListing.to_json())

# convert the object into a dict
ssh_key_full_listing_dict = ssh_key_full_listing_instance.to_dict()
# create an instance of SshKeyFullListing from a dict
ssh_key_full_listing_from_dict = SshKeyFullListing.from_dict(ssh_key_full_listing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


