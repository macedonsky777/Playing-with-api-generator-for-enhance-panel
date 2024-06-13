# LoginsListing


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[Login]**](Login.md) |  | 
**total** | **int** |  | 

## Example

```python
from openapi_client.models.logins_listing import LoginsListing

# TODO update the JSON string below
json = "{}"
# create an instance of LoginsListing from a JSON string
logins_listing_instance = LoginsListing.from_json(json)
# print the JSON string representation of the object
print(LoginsListing.to_json())

# convert the object into a dict
logins_listing_dict = logins_listing_instance.to_dict()
# create an instance of LoginsListing from a dict
logins_listing_from_dict = LoginsListing.from_dict(logins_listing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


