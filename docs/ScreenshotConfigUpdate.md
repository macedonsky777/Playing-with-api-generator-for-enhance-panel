# ScreenshotConfigUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enable** | **bool** |  | [optional] 
**interval** | [**Int**](Int.md) |  | [optional] 

## Example

```python
from openapi_client.models.screenshot_config_update import ScreenshotConfigUpdate

# TODO update the JSON string below
json = "{}"
# create an instance of ScreenshotConfigUpdate from a JSON string
screenshot_config_update_instance = ScreenshotConfigUpdate.from_json(json)
# print the JSON string representation of the object
print(ScreenshotConfigUpdate.to_json())

# convert the object into a dict
screenshot_config_update_dict = screenshot_config_update_instance.to_dict()
# create an instance of ScreenshotConfigUpdate from a dict
screenshot_config_update_from_dict = ScreenshotConfigUpdate.from_dict(screenshot_config_update_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


