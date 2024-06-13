# IniSetting


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** |  | 
**value** | **str** |  | 
**section** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.ini_setting import IniSetting

# TODO update the JSON string below
json = "{}"
# create an instance of IniSetting from a JSON string
ini_setting_instance = IniSetting.from_json(json)
# print the JSON string representation of the object
print(IniSetting.to_json())

# convert the object into a dict
ini_setting_dict = ini_setting_instance.to_dict()
# create an instance of IniSetting from a dict
ini_setting_from_dict = IniSetting.from_dict(ini_setting_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


