# ImporterAnalyzedDataMysqlGrantsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**db_name** | **str** |  | 
**username** | **str** |  | 
**table_name** | **str** |  | 
**privilege** | **List[str]** |  | [optional] 

## Example

```python
from openapi_client.models.importer_analyzed_data_mysql_grants_inner import ImporterAnalyzedDataMysqlGrantsInner

# TODO update the JSON string below
json = "{}"
# create an instance of ImporterAnalyzedDataMysqlGrantsInner from a JSON string
importer_analyzed_data_mysql_grants_inner_instance = ImporterAnalyzedDataMysqlGrantsInner.from_json(json)
# print the JSON string representation of the object
print(ImporterAnalyzedDataMysqlGrantsInner.to_json())

# convert the object into a dict
importer_analyzed_data_mysql_grants_inner_dict = importer_analyzed_data_mysql_grants_inner_instance.to_dict()
# create an instance of ImporterAnalyzedDataMysqlGrantsInner from a dict
importer_analyzed_data_mysql_grants_inner_from_dict = ImporterAnalyzedDataMysqlGrantsInner.from_dict(importer_analyzed_data_mysql_grants_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


