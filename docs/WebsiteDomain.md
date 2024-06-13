# WebsiteDomain


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**domain** | **str** |  | 
**document_root** | **str** |  | 
**kind** | [**DomainMappingKind**](DomainMappingKind.md) |  | 
**cloudflare_status** | [**CloudFlareStatus**](CloudFlareStatus.md) |  | 

## Example

```python
from openapi_client.models.website_domain import WebsiteDomain

# TODO update the JSON string below
json = "{}"
# create an instance of WebsiteDomain from a JSON string
website_domain_instance = WebsiteDomain.from_json(json)
# print the JSON string representation of the object
print(WebsiteDomain.to_json())

# convert the object into a dict
website_domain_dict = website_domain_instance.to_dict()
# create an instance of WebsiteDomain from a dict
website_domain_from_dict = WebsiteDomain.from_dict(website_domain_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


