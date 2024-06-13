# DatabaseRoleInfo


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**state** | [**ServerRoleState**](ServerRoleState.md) |  | 
**usage** | **int** |  | 
**mysql_stats** | **object** |  | 
**mysqlcd** | [**ServiceInfo**](ServiceInfo.md) |  | 
**websites_count** | **int** | The number of websites whose databases are assigned to be on this database role. | 

## Example

```python
from openapi_client.models.database_role_info import DatabaseRoleInfo

# TODO update the JSON string below
json = "{}"
# create an instance of DatabaseRoleInfo from a JSON string
database_role_info_instance = DatabaseRoleInfo.from_json(json)
# print the JSON string representation of the object
print(DatabaseRoleInfo.to_json())

# convert the object into a dict
database_role_info_dict = database_role_info_instance.to_dict()
# create an instance of DatabaseRoleInfo from a dict
database_role_info_from_dict = DatabaseRoleInfo.from_dict(database_role_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


