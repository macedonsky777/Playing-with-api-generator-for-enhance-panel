# WpInstallation


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**db_name** | **str** |  | 
**db_user** | **str** |  | 
**table_prefix** | **str** |  | 
**path** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.wp_installation import WpInstallation

# TODO update the JSON string below
json = "{}"
# create an instance of WpInstallation from a JSON string
wp_installation_instance = WpInstallation.from_json(json)
# print the JSON string representation of the object
print(WpInstallation.to_json())

# convert the object into a dict
wp_installation_dict = wp_installation_instance.to_dict()
# create an instance of WpInstallation from a dict
wp_installation_from_dict = WpInstallation.from_dict(wp_installation_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


