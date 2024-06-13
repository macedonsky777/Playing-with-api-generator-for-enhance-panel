# UpdateWpPlugin


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | [**WPPluginStatus**](WPPluginStatus.md) |  | [optional] 
**auto_update** | [**WPPluginAutoUpdateStatus**](WPPluginAutoUpdateStatus.md) |  | [optional] 

## Example

```python
from openapi_client.models.update_wp_plugin import UpdateWpPlugin

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateWpPlugin from a JSON string
update_wp_plugin_instance = UpdateWpPlugin.from_json(json)
# print the JSON string representation of the object
print(UpdateWpPlugin.to_json())

# convert the object into a dict
update_wp_plugin_dict = update_wp_plugin_instance.to_dict()
# create an instance of UpdateWpPlugin from a dict
update_wp_plugin_from_dict = UpdateWpPlugin.from_dict(update_wp_plugin_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


