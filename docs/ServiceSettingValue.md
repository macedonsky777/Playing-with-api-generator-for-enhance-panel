# ServiceSettingValue


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**host** | [**SmartHostSettingsHost**](SmartHostSettingsHost.md) |  | 
**creds** | [**SmartHostSettingsCreds**](SmartHostSettingsCreds.md) |  | 

## Example

```python
from openapi_client.models.service_setting_value import ServiceSettingValue

# TODO update the JSON string below
json = "{}"
# create an instance of ServiceSettingValue from a JSON string
service_setting_value_instance = ServiceSettingValue.from_json(json)
# print the JSON string representation of the object
print(ServiceSettingValue.to_json())

# convert the object into a dict
service_setting_value_dict = service_setting_value_instance.to_dict()
# create an instance of ServiceSettingValue from a dict
service_setting_value_from_dict = ServiceSettingValue.from_dict(service_setting_value_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


