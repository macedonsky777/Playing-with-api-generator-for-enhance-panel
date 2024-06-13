# InstallWpThemeRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**activate** | **bool** | Activate theme after installation | [optional] 

## Example

```python
from openapi_client.models.install_wp_theme_request import InstallWpThemeRequest

# TODO update the JSON string below
json = "{}"
# create an instance of InstallWpThemeRequest from a JSON string
install_wp_theme_request_instance = InstallWpThemeRequest.from_json(json)
# print the JSON string representation of the object
print(InstallWpThemeRequest.to_json())

# convert the object into a dict
install_wp_theme_request_dict = install_wp_theme_request_instance.to_dict()
# create an instance of InstallWpThemeRequest from a dict
install_wp_theme_request_from_dict = InstallWpThemeRequest.from_dict(install_wp_theme_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


