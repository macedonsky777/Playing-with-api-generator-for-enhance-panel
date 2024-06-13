# MySQLDB


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**name** | **str** |  | 
**server_id** | **str** |  | [optional] 
**website_id** | **str** |  | 
**size** | **int** |  | 
**created_at** | **str** |  | 

## Example

```python
from openapi_client.models.my_sqldb import MySQLDB

# TODO update the JSON string below
json = "{}"
# create an instance of MySQLDB from a JSON string
my_sqldb_instance = MySQLDB.from_json(json)
# print the JSON string representation of the object
print(MySQLDB.to_json())

# convert the object into a dict
my_sqldb_dict = my_sqldb_instance.to_dict()
# create an instance of MySQLDB from a dict
my_sqldb_from_dict = MySQLDB.from_dict(my_sqldb_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


