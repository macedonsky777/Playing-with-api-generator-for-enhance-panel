# WebsiteServerDomains


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**app_server_domains** | **List[str]** |  | 
**email_server_domains** | **List[str]** |  | [optional] 
**db_server_domains** | **List[str]** |  | [optional] 

## Example

```python
from openapi_client.models.website_server_domains import WebsiteServerDomains

# TODO update the JSON string below
json = "{}"
# create an instance of WebsiteServerDomains from a JSON string
website_server_domains_instance = WebsiteServerDomains.from_json(json)
# print the JSON string representation of the object
print(WebsiteServerDomains.to_json())

# convert the object into a dict
website_server_domains_dict = website_server_domains_instance.to_dict()
# create an instance of WebsiteServerDomains from a dict
website_server_domains_from_dict = WebsiteServerDomains.from_dict(website_server_domains_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


