# WpPlugin

Describes the filename and additional plugin information. The filename is the name of the plugin php file, e.g. \"bbpress.php\". If the plugin kind is \"file\", then the file name refers to e.g. \"wp-content/plugins/bbpress.php\". If the kind is \"dir\", then the name refers to \"wp-content/plugins/bbpress/bbpress.php\". The name of the dir is always the same as the name of the file without the php suffix. https://developer.wordpress.org/plugins/plugin-basics/header-requirements/#header-fields

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**uri** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**version** | **str** |  | 
**update** | [**WPPluginUpdateAvailable**](WPPluginUpdateAvailable.md) |  | [optional] 
**auto_update** | [**WPPluginAutoUpdateStatus**](WPPluginAutoUpdateStatus.md) |  | [optional] 
**status** | [**WPPluginStatus**](WPPluginStatus.md) |  | [optional] 
**author** | **str** |  | 

## Example

```python
from openapi_client.models.wp_plugin import WpPlugin

# TODO update the JSON string below
json = "{}"
# create an instance of WpPlugin from a JSON string
wp_plugin_instance = WpPlugin.from_json(json)
# print the JSON string representation of the object
print(WpPlugin.to_json())

# convert the object into a dict
wp_plugin_dict = wp_plugin_instance.to_dict()
# create an instance of WpPlugin from a dict
wp_plugin_from_dict = WpPlugin.from_dict(wp_plugin_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


