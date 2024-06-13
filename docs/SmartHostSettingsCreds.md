# SmartHostSettingsCreds


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**username** | **str** |  | 
**password** | **str** |  | 

## Example

```python
from openapi_client.models.smart_host_settings_creds import SmartHostSettingsCreds

# TODO update the JSON string below
json = "{}"
# create an instance of SmartHostSettingsCreds from a JSON string
smart_host_settings_creds_instance = SmartHostSettingsCreds.from_json(json)
# print the JSON string representation of the object
print(SmartHostSettingsCreds.to_json())

# convert the object into a dict
smart_host_settings_creds_dict = smart_host_settings_creds_instance.to_dict()
# create an instance of SmartHostSettingsCreds from a dict
smart_host_settings_creds_from_dict = SmartHostSettingsCreds.from_dict(smart_host_settings_creds_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


