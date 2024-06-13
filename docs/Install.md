# Install


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**owner** | [**LoginInfo**](LoginInfo.md) |  | 
**org_name** | **str** |  | [optional] 
**accept_terms** | **bool** |  | [optional] 
**locale** | [**CPLocale**](CPLocale.md) |  | 

## Example

```python
from openapi_client.models.install import Install

# TODO update the JSON string below
json = "{}"
# create an instance of Install from a JSON string
install_instance = Install.from_json(json)
# print the JSON string representation of the object
print(Install.to_json())

# convert the object into a dict
install_dict = install_instance.to_dict()
# create an instance of Install from a dict
install_from_dict = Install.from_dict(install_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


