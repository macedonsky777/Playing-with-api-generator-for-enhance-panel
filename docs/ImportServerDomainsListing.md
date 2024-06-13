# ImportServerDomainsListing


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total** | **int** |  | 
**items** | [**List[ImportServerDomain]**](ImportServerDomain.md) |  | 

## Example

```python
from openapi_client.models.import_server_domains_listing import ImportServerDomainsListing

# TODO update the JSON string below
json = "{}"
# create an instance of ImportServerDomainsListing from a JSON string
import_server_domains_listing_instance = ImportServerDomainsListing.from_json(json)
# print the JSON string representation of the object
print(ImportServerDomainsListing.to_json())

# convert the object into a dict
import_server_domains_listing_dict = import_server_domains_listing_instance.to_dict()
# create an instance of ImportServerDomainsListing from a dict
import_server_domains_listing_from_dict = ImportServerDomainsListing.from_dict(import_server_domains_listing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


