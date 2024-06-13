# ServerStatsFullListing


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[ServerStatEntry]**](ServerStatEntry.md) |  | 

## Example

```python
from openapi_client.models.server_stats_full_listing import ServerStatsFullListing

# TODO update the JSON string below
json = "{}"
# create an instance of ServerStatsFullListing from a JSON string
server_stats_full_listing_instance = ServerStatsFullListing.from_json(json)
# print the JSON string representation of the object
print(ServerStatsFullListing.to_json())

# convert the object into a dict
server_stats_full_listing_dict = server_stats_full_listing_instance.to_dict()
# create an instance of ServerStatsFullListing from a dict
server_stats_full_listing_from_dict = ServerStatsFullListing.from_dict(server_stats_full_listing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


