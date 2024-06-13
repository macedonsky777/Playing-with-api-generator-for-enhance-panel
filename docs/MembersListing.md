# MembersListing


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[Member]**](Member.md) |  | 
**total** | **int** |  | 

## Example

```python
from openapi_client.models.members_listing import MembersListing

# TODO update the JSON string below
json = "{}"
# create an instance of MembersListing from a JSON string
members_listing_instance = MembersListing.from_json(json)
# print the JSON string representation of the object
print(MembersListing.to_json())

# convert the object into a dict
members_listing_dict = members_listing_instance.to_dict()
# create an instance of MembersListing from a dict
members_listing_from_dict = MembersListing.from_dict(members_listing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


