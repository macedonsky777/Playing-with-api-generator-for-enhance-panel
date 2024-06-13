# WebsitePhpSettings


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**website_id** | **str** |  | 
**php_ini** | [**PhpIni**](PhpIni.md) |  | 

## Example

```python
from openapi_client.models.website_php_settings import WebsitePhpSettings

# TODO update the JSON string below
json = "{}"
# create an instance of WebsitePhpSettings from a JSON string
website_php_settings_instance = WebsitePhpSettings.from_json(json)
# print the JSON string representation of the object
print(WebsitePhpSettings.to_json())

# convert the object into a dict
website_php_settings_dict = website_php_settings_instance.to_dict()
# create an instance of WebsitePhpSettings from a dict
website_php_settings_from_dict = WebsitePhpSettings.from_dict(website_php_settings_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


