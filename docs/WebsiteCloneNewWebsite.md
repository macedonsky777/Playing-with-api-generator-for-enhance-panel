# WebsiteCloneNewWebsite


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **str** | The domain of the new website. | 
**subscription_id** | **int** |  | [optional] 
**app_server_id** | **str** |  | [optional] 
**backup_server_id** | **str** |  | [optional] 
**db_server_id** | **str** |  | [optional] 
**email_server_id** | **str** |  | [optional] 
**server_group_id** | **str** |  | [optional] 
**php_version** | [**PhpVersion**](PhpVersion.md) |  | [optional] 
**kind** | [**WebsiteKind**](WebsiteKind.md) |  | [optional] 

## Example

```python
from openapi_client.models.website_clone_new_website import WebsiteCloneNewWebsite

# TODO update the JSON string below
json = "{}"
# create an instance of WebsiteCloneNewWebsite from a JSON string
website_clone_new_website_instance = WebsiteCloneNewWebsite.from_json(json)
# print the JSON string representation of the object
print(WebsiteCloneNewWebsite.to_json())

# convert the object into a dict
website_clone_new_website_dict = website_clone_new_website_instance.to_dict()
# create an instance of WebsiteCloneNewWebsite from a dict
website_clone_new_website_from_dict = WebsiteCloneNewWebsite.from_dict(website_clone_new_website_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


