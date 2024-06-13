# ImporterAnalyzedDataMysqlUsersInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**username** | **str** |  | 
**auth_plugin** | **str** |  | 

## Example

```python
from openapi_client.models.importer_analyzed_data_mysql_users_inner import ImporterAnalyzedDataMysqlUsersInner

# TODO update the JSON string below
json = "{}"
# create an instance of ImporterAnalyzedDataMysqlUsersInner from a JSON string
importer_analyzed_data_mysql_users_inner_instance = ImporterAnalyzedDataMysqlUsersInner.from_json(json)
# print the JSON string representation of the object
print(ImporterAnalyzedDataMysqlUsersInner.to_json())

# convert the object into a dict
importer_analyzed_data_mysql_users_inner_dict = importer_analyzed_data_mysql_users_inner_instance.to_dict()
# create an instance of ImporterAnalyzedDataMysqlUsersInner from a dict
importer_analyzed_data_mysql_users_inner_from_dict = ImporterAnalyzedDataMysqlUsersInner.from_dict(importer_analyzed_data_mysql_users_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


