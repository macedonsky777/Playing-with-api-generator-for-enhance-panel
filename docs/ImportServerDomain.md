# ImportServerDomain


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**import_server_id** | **str** |  | 
**domain** | **str** |  | 
**kind** | [**DomainMappingKind**](DomainMappingKind.md) |  | 
**user** | **str** |  | 
**movable** | **bool** |  | 

## Example

```python
from openapi_client.models.import_server_domain import ImportServerDomain

# TODO update the JSON string below
json = "{}"
# create an instance of ImportServerDomain from a JSON string
import_server_domain_instance = ImportServerDomain.from_json(json)
# print the JSON string representation of the object
print(ImportServerDomain.to_json())

# convert the object into a dict
import_server_domain_dict = import_server_domain_instance.to_dict()
# create an instance of ImportServerDomain from a dict
import_server_domain_from_dict = ImportServerDomain.from_dict(import_server_domain_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


