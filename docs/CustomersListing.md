# CustomersListing


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[Org]**](Org.md) |  | 
**total** | **int** |  | 

## Example

```python
from openapi_client.models.customers_listing import CustomersListing

# TODO update the JSON string below
json = "{}"
# create an instance of CustomersListing from a JSON string
customers_listing_instance = CustomersListing.from_json(json)
# print the JSON string representation of the object
print(CustomersListing.to_json())

# convert the object into a dict
customers_listing_dict = customers_listing_instance.to_dict()
# create an instance of CustomersListing from a dict
customers_listing_from_dict = CustomersListing.from_dict(customers_listing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


