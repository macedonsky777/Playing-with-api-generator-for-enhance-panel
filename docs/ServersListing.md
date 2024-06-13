# ServersListing


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[ServerInfoBrief]**](ServerInfoBrief.md) |  | 
**total** | **int** |  | 

## Example

```python
from openapi_client.models.servers_listing import ServersListing

# TODO update the JSON string below
json = "{}"
# create an instance of ServersListing from a JSON string
servers_listing_instance = ServersListing.from_json(json)
# print the JSON string representation of the object
print(ServersListing.to_json())

# convert the object into a dict
servers_listing_dict = servers_listing_instance.to_dict()
# create an instance of ServersListing from a dict
servers_listing_from_dict = ServersListing.from_dict(servers_listing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


