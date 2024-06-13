# NewMySQLUser


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**username** | **str** |  | 
**password** | **str** |  | 
**auth_plugin** | [**MySQLAuthPlugin**](MySQLAuthPlugin.md) |  | [optional] 

## Example

```python
from openapi_client.models.new_my_sql_user import NewMySQLUser

# TODO update the JSON string below
json = "{}"
# create an instance of NewMySQLUser from a JSON string
new_my_sql_user_instance = NewMySQLUser.from_json(json)
# print the JSON string representation of the object
print(NewMySQLUser.to_json())

# convert the object into a dict
new_my_sql_user_dict = new_my_sql_user_instance.to_dict()
# create an instance of NewMySQLUser from a dict
new_my_sql_user_from_dict = NewMySQLUser.from_dict(new_my_sql_user_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


