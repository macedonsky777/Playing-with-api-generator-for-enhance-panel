# ImporterAnalyzedData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domains** | [**List[ImporterAnalyzedDataDomainsInner]**](ImporterAnalyzedDataDomainsInner.md) |  | 
**mysql_databases** | [**List[ImporterAnalyzedDataMysqlDatabasesInner]**](ImporterAnalyzedDataMysqlDatabasesInner.md) |  | [optional] 
**mysql_users** | [**List[ImporterAnalyzedDataMysqlUsersInner]**](ImporterAnalyzedDataMysqlUsersInner.md) |  | [optional] 
**mysql_grants** | [**List[ImporterAnalyzedDataMysqlGrantsInner]**](ImporterAnalyzedDataMysqlGrantsInner.md) |  | [optional] 
**crontabs** | [**List[ImporterAnalyzedDataCrontabsInner]**](ImporterAnalyzedDataCrontabsInner.md) |  | [optional] 
**ftps** | [**List[ImporterAnalyzedDataFtpsInner]**](ImporterAnalyzedDataFtpsInner.md) |  | [optional] 
**mailboxes** | [**List[ImporterAnalyzedDataMailboxesInner]**](ImporterAnalyzedDataMailboxesInner.md) |  | [optional] 

## Example

```python
from openapi_client.models.importer_analyzed_data import ImporterAnalyzedData

# TODO update the JSON string below
json = "{}"
# create an instance of ImporterAnalyzedData from a JSON string
importer_analyzed_data_instance = ImporterAnalyzedData.from_json(json)
# print the JSON string representation of the object
print(ImporterAnalyzedData.to_json())

# convert the object into a dict
importer_analyzed_data_dict = importer_analyzed_data_instance.to_dict()
# create an instance of ImporterAnalyzedData from a dict
importer_analyzed_data_from_dict = ImporterAnalyzedData.from_dict(importer_analyzed_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


