# WpDebug

Enable or disable debug mode.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**wp_debug** | **bool** |  | 

## Example

```python
from openapi_client.models.wp_debug import WpDebug

# TODO update the JSON string below
json = "{}"
# create an instance of WpDebug from a JSON string
wp_debug_instance = WpDebug.from_json(json)
# print the JSON string representation of the object
print(WpDebug.to_json())

# convert the object into a dict
wp_debug_dict = wp_debug_instance.to_dict()
# create an instance of WpDebug from a dict
wp_debug_from_dict = WpDebug.from_dict(wp_debug_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


