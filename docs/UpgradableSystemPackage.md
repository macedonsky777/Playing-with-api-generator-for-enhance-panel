# UpgradableSystemPackage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | [**SystemPackageName**](SystemPackageName.md) |  | 
**version** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.upgradable_system_package import UpgradableSystemPackage

# TODO update the JSON string below
json = "{}"
# create an instance of UpgradableSystemPackage from a JSON string
upgradable_system_package_instance = UpgradableSystemPackage.from_json(json)
# print the JSON string representation of the object
print(UpgradableSystemPackage.to_json())

# convert the object into a dict
upgradable_system_package_dict = upgradable_system_package_instance.to_dict()
# create an instance of UpgradableSystemPackage from a dict
upgradable_system_package_from_dict = UpgradableSystemPackage.from_dict(upgradable_system_package_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


