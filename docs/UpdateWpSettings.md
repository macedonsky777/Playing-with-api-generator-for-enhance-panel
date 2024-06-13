# UpdateWpSettings


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**auto_update_core** | [**WPAutoUpdateCore**](WPAutoUpdateCore.md) |  | [optional] 
**disallow_non_wp_php** | **bool** |  | [optional] 
**login_access** | **List[str]** |  | [optional] 

## Example

```python
from openapi_client.models.update_wp_settings import UpdateWpSettings

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateWpSettings from a JSON string
update_wp_settings_instance = UpdateWpSettings.from_json(json)
# print the JSON string representation of the object
print(UpdateWpSettings.to_json())

# convert the object into a dict
update_wp_settings_dict = update_wp_settings_instance.to_dict()
# create an instance of UpdateWpSettings from a dict
update_wp_settings_from_dict = UpdateWpSettings.from_dict(update_wp_settings_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


