# WebsitesListing


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[Website]**](Website.md) |  | 
**total** | **int** |  | 

## Example

```python
from openapi_client.models.websites_listing import WebsitesListing

# TODO update the JSON string below
json = "{}"
# create an instance of WebsitesListing from a JSON string
websites_listing_instance = WebsitesListing.from_json(json)
# print the JSON string representation of the object
print(WebsitesListing.to_json())

# convert the object into a dict
websites_listing_dict = websites_listing_instance.to_dict()
# create an instance of WebsitesListing from a dict
websites_listing_from_dict = WebsitesListing.from_dict(websites_listing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


