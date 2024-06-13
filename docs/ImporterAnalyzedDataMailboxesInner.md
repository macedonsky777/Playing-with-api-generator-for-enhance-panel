# ImporterAnalyzedDataMailboxesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**username** | **str** |  | 
**domain** | **str** |  | 
**has_mailbox** | **bool** |  | 
**is_suspended** | **bool** |  | 
**forwarders** | **List[str]** |  | [optional] 
**quota** | **float** |  | [optional] 

## Example

```python
from openapi_client.models.importer_analyzed_data_mailboxes_inner import ImporterAnalyzedDataMailboxesInner

# TODO update the JSON string below
json = "{}"
# create an instance of ImporterAnalyzedDataMailboxesInner from a JSON string
importer_analyzed_data_mailboxes_inner_instance = ImporterAnalyzedDataMailboxesInner.from_json(json)
# print the JSON string representation of the object
print(ImporterAnalyzedDataMailboxesInner.to_json())

# convert the object into a dict
importer_analyzed_data_mailboxes_inner_dict = importer_analyzed_data_mailboxes_inner_instance.to_dict()
# create an instance of ImporterAnalyzedDataMailboxesInner from a dict
importer_analyzed_data_mailboxes_inner_from_dict = ImporterAnalyzedDataMailboxesInner.from_dict(importer_analyzed_data_mailboxes_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


