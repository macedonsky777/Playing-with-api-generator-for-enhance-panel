# ScreenshotConfig


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**is_enabled** | **bool** |  | 
**interval** | [**Int**](Int.md) |  | [optional] 

## Example

```python
from openapi_client.models.screenshot_config import ScreenshotConfig

# TODO update the JSON string below
json = "{}"
# create an instance of ScreenshotConfig from a JSON string
screenshot_config_instance = ScreenshotConfig.from_json(json)
# print the JSON string representation of the object
print(ScreenshotConfig.to_json())

# convert the object into a dict
screenshot_config_dict = screenshot_config_instance.to_dict()
# create an instance of ScreenshotConfig from a dict
screenshot_config_from_dict = ScreenshotConfig.from_dict(screenshot_config_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


