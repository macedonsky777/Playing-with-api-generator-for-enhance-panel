# SmartHostSettings


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**host** | [**SmartHostSettingsHost**](SmartHostSettingsHost.md) |  | 
**creds** | [**SmartHostSettingsCreds**](SmartHostSettingsCreds.md) |  | 

## Example

```python
from openapi_client.models.smart_host_settings import SmartHostSettings

# TODO update the JSON string below
json = "{}"
# create an instance of SmartHostSettings from a JSON string
smart_host_settings_instance = SmartHostSettings.from_json(json)
# print the JSON string representation of the object
print(SmartHostSettings.to_json())

# convert the object into a dict
smart_host_settings_dict = smart_host_settings_instance.to_dict()
# create an instance of SmartHostSettings from a dict
smart_host_settings_from_dict = SmartHostSettings.from_dict(smart_host_settings_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


