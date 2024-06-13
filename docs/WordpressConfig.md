# WordpressConfig


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**wp_debug** | **bool** |  | 
**wp_debug_log** | **bool** |  | 
**wp_debug_display** | **bool** |  | 

## Example

```python
from openapi_client.models.wordpress_config import WordpressConfig

# TODO update the JSON string below
json = "{}"
# create an instance of WordpressConfig from a JSON string
wordpress_config_instance = WordpressConfig.from_json(json)
# print the JSON string representation of the object
print(WordpressConfig.to_json())

# convert the object into a dict
wordpress_config_dict = wordpress_config_instance.to_dict()
# create an instance of WordpressConfig from a dict
wordpress_config_from_dict = WordpressConfig.from_dict(wordpress_config_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


