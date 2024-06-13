# MySQLDBsListing


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[MySQLDB]**](MySQLDB.md) |  | 

## Example

```python
from openapi_client.models.my_sqldbs_listing import MySQLDBsListing

# TODO update the JSON string below
json = "{}"
# create an instance of MySQLDBsListing from a JSON string
my_sqldbs_listing_instance = MySQLDBsListing.from_json(json)
# print the JSON string representation of the object
print(MySQLDBsListing.to_json())

# convert the object into a dict
my_sqldbs_listing_dict = my_sqldbs_listing_instance.to_dict()
# create an instance of MySQLDBsListing from a dict
my_sqldbs_listing_from_dict = MySQLDBsListing.from_dict(my_sqldbs_listing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


