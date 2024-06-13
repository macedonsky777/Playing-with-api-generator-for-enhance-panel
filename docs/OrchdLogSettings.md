# OrchdLogSettings

Settings for orchd logging

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**limit** | [**LogLevelLimit**](LogLevelLimit.md) |  | 

## Example

```python
from openapi_client.models.orchd_log_settings import OrchdLogSettings

# TODO update the JSON string below
json = "{}"
# create an instance of OrchdLogSettings from a JSON string
orchd_log_settings_instance = OrchdLogSettings.from_json(json)
# print the JSON string representation of the object
print(OrchdLogSettings.to_json())

# convert the object into a dict
orchd_log_settings_dict = orchd_log_settings_instance.to_dict()
# create an instance of OrchdLogSettings from a dict
orchd_log_settings_from_dict = OrchdLogSettings.from_dict(orchd_log_settings_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


