# WpSettings


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**auto_update_core** | [**WPAutoUpdateCore**](WPAutoUpdateCore.md) |  | [optional] 
**disallow_non_wp_php** | **bool** |  | 
**login_access** | **List[str]** |  | 

## Example

```python
from openapi_client.models.wp_settings import WpSettings

# TODO update the JSON string below
json = "{}"
# create an instance of WpSettings from a JSON string
wp_settings_instance = WpSettings.from_json(json)
# print the JSON string representation of the object
print(WpSettings.to_json())

# convert the object into a dict
wp_settings_dict = wp_settings_instance.to_dict()
# create an instance of WpSettings from a dict
wp_settings_from_dict = WpSettings.from_dict(wp_settings_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


