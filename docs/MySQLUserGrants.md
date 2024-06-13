# MySQLUserGrants


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**db_id** | **str** |  | 
**grants** | **List[str]** |  | 

## Example

```python
from openapi_client.models.my_sql_user_grants import MySQLUserGrants

# TODO update the JSON string below
json = "{}"
# create an instance of MySQLUserGrants from a JSON string
my_sql_user_grants_instance = MySQLUserGrants.from_json(json)
# print the JSON string representation of the object
print(MySQLUserGrants.to_json())

# convert the object into a dict
my_sql_user_grants_dict = my_sql_user_grants_instance.to_dict()
# create an instance of MySQLUserGrants from a dict
my_sql_user_grants_from_dict = MySQLUserGrants.from_dict(my_sql_user_grants_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


