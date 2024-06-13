# WpTheme

Describes the theme directory name and additional theme information.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**status** | [**WPPluginStatus**](WPPluginStatus.md) |  | 
**version** | **str** |  | 
**update** | **str** |  | [optional] 
**auto_update** | [**WPThemeAutoUpdateStatus**](WPThemeAutoUpdateStatus.md) |  | [optional] 

## Example

```python
from openapi_client.models.wp_theme import WpTheme

# TODO update the JSON string below
json = "{}"
# create an instance of WpTheme from a JSON string
wp_theme_instance = WpTheme.from_json(json)
# print the JSON string representation of the object
print(WpTheme.to_json())

# convert the object into a dict
wp_theme_dict = wp_theme_instance.to_dict()
# create an instance of WpTheme from a dict
wp_theme_from_dict = WpTheme.from_dict(wp_theme_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


