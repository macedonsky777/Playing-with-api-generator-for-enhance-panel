# Branding


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**org_name** | **str** |  | 
**parent** | **str** |  | [optional] 
**control_panel_domain** | **str** |  | [optional] 
**php_my_admin_domain** | **str** |  | [optional] 
**roundcube_domain** | **str** |  | [optional] 
**logo_path** | **str** |  | [optional] 
**inverse_logo_path** | **str** |  | [optional] 
**inverse_icon_path** | **str** |  | [optional] 
**login_image_path** | **str** |  | [optional] 
**favicon_path** | **str** |  | [optional] 
**name_servers** | **List[str]** |  | [optional] 
**settings** | [**List[Setting]**](Setting.md) |  | 
**staging_domain** | **str** |  | [optional] 
**locale** | [**CPLocale**](CPLocale.md) |  | 

## Example

```python
from openapi_client.models.branding import Branding

# TODO update the JSON string below
json = "{}"
# create an instance of Branding from a JSON string
branding_instance = Branding.from_json(json)
# print the JSON string representation of the object
print(Branding.to_json())

# convert the object into a dict
branding_dict = branding_instance.to_dict()
# create an instance of Branding from a dict
branding_from_dict = Branding.from_dict(branding_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


