# MySQLUsersFullListing


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[MySQLUser]**](MySQLUser.md) |  | 

## Example

```python
from openapi_client.models.my_sql_users_full_listing import MySQLUsersFullListing

# TODO update the JSON string below
json = "{}"
# create an instance of MySQLUsersFullListing from a JSON string
my_sql_users_full_listing_instance = MySQLUsersFullListing.from_json(json)
# print the JSON string representation of the object
print(MySQLUsersFullListing.to_json())

# convert the object into a dict
my_sql_users_full_listing_dict = my_sql_users_full_listing_instance.to_dict()
# create an instance of MySQLUsersFullListing from a dict
my_sql_users_full_listing_from_dict = MySQLUsersFullListing.from_dict(my_sql_users_full_listing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


