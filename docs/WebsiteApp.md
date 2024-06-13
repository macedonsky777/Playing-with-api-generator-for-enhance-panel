# WebsiteApp


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**app** | [**WebsiteAppKind**](WebsiteAppKind.md) |  | 
**path** | **str** | The path is only present if the app is installed in the root instead of a subfolder. For example if a customer installs Wordpress at &#39;/blog&#39;, then the path will be present and equal to &#39;blog&#39;. But if they install WP in website root, instead of returning &#39;/&#39; or empty string, this property is omitted. | [optional] 
**default_wp_user_id** | **int** | Only present if default was set by the user. Otherwise, this field isn&#39;t there. | [optional] 

## Example

```python
from openapi_client.models.website_app import WebsiteApp

# TODO update the JSON string below
json = "{}"
# create an instance of WebsiteApp from a JSON string
website_app_instance = WebsiteApp.from_json(json)
# print the JSON string representation of the object
print(WebsiteApp.to_json())

# convert the object into a dict
website_app_dict = website_app_instance.to_dict()
# create an instance of WebsiteApp from a dict
website_app_from_dict = WebsiteApp.from_dict(website_app_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


