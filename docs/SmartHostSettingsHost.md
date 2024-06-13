# SmartHostSettingsHost


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**hostname** | **str** |  | 
**port** | **int** |  | [optional] 

## Example

```python
from openapi_client.models.smart_host_settings_host import SmartHostSettingsHost

# TODO update the JSON string below
json = "{}"
# create an instance of SmartHostSettingsHost from a JSON string
smart_host_settings_host_instance = SmartHostSettingsHost.from_json(json)
# print the JSON string representation of the object
print(SmartHostSettingsHost.to_json())

# convert the object into a dict
smart_host_settings_host_dict = smart_host_settings_host_instance.to_dict()
# create an instance of SmartHostSettingsHost from a dict
smart_host_settings_host_from_dict = SmartHostSettingsHost.from_dict(smart_host_settings_host_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


