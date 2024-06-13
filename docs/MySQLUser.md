# MySQLUser


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**db_id** | **str** |  | [optional] 
**username** | **str** |  | 
**access_hosts** | **List[str]** |  | 
**auth_plugin** | [**MySQLAuthPlugin**](MySQLAuthPlugin.md) |  | 
**grants** | **object** | Table names mapped to a list of privileges on that table. The wildcard \&quot;*\&quot; means the privileges are granted for all tables. | 
**created_at** | **str** |  | 
**is_ephemeral** | **bool** | A flag which marks short-lived mysql accounts. If an account is created as ephemeral, it will be deleted few hours after it&#39;s been created. Throwaway accounts are useful for phpMyAdmin logins. | [optional] [default to False]

## Example

```python
from openapi_client.models.my_sql_user import MySQLUser

# TODO update the JSON string below
json = "{}"
# create an instance of MySQLUser from a JSON string
my_sql_user_instance = MySQLUser.from_json(json)
# print the JSON string representation of the object
print(MySQLUser.to_json())

# convert the object into a dict
my_sql_user_dict = my_sql_user_instance.to_dict()
# create an instance of MySQLUser from a dict
my_sql_user_from_dict = MySQLUser.from_dict(my_sql_user_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


