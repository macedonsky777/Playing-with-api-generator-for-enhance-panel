# DomainsListing


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[Domain]**](Domain.md) |  | 
**total** | **int** |  | 

## Example

```python
from openapi_client.models.domains_listing import DomainsListing

# TODO update the JSON string below
json = "{}"
# create an instance of DomainsListing from a JSON string
domains_listing_instance = DomainsListing.from_json(json)
# print the JSON string representation of the object
print(DomainsListing.to_json())

# convert the object into a dict
domains_listing_dict = domains_listing_instance.to_dict()
# create an instance of DomainsListing from a dict
domains_listing_from_dict = DomainsListing.from_dict(domains_listing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


