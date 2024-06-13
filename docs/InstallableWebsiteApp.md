# InstallableWebsiteApp


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**app** | [**WebsiteAppKind**](WebsiteAppKind.md) |  | 
**version** | **str** |  | 
**is_latest** | **bool** |  | 
**description** | **str** |  | [optional] 
**size** | **float** | Approximate number of bytes after fresh installation. | [optional] 
**created_at** | **datetime** |  | 

## Example

```python
from openapi_client.models.installable_website_app import InstallableWebsiteApp

# TODO update the JSON string below
json = "{}"
# create an instance of InstallableWebsiteApp from a JSON string
installable_website_app_instance = InstallableWebsiteApp.from_json(json)
# print the JSON string representation of the object
print(InstallableWebsiteApp.to_json())

# convert the object into a dict
installable_website_app_dict = installable_website_app_instance.to_dict()
# create an instance of InstallableWebsiteApp from a dict
installable_website_app_from_dict = InstallableWebsiteApp.from_dict(installable_website_app_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


