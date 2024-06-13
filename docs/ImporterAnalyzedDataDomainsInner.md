# ImporterAnalyzedDataDomainsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain_name** | **str** |  | 
**domain_kind** | **str** |  | 
**php_version** | **str** |  | [optional] 
**document_root** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.importer_analyzed_data_domains_inner import ImporterAnalyzedDataDomainsInner

# TODO update the JSON string below
json = "{}"
# create an instance of ImporterAnalyzedDataDomainsInner from a JSON string
importer_analyzed_data_domains_inner_instance = ImporterAnalyzedDataDomainsInner.from_json(json)
# print the JSON string representation of the object
print(ImporterAnalyzedDataDomainsInner.to_json())

# convert the object into a dict
importer_analyzed_data_domains_inner_dict = importer_analyzed_data_domains_inner_instance.to_dict()
# create an instance of ImporterAnalyzedDataDomainsInner from a dict
importer_analyzed_data_domains_inner_from_dict = ImporterAnalyzedDataDomainsInner.from_dict(importer_analyzed_data_domains_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


