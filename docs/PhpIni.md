# PhpIni


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[IniSetting]**](IniSetting.md) |  | 

## Example

```python
from openapi_client.models.php_ini import PhpIni

# TODO update the JSON string below
json = "{}"
# create an instance of PhpIni from a JSON string
php_ini_instance = PhpIni.from_json(json)
# print the JSON string representation of the object
print(PhpIni.to_json())

# convert the object into a dict
php_ini_dict = php_ini_instance.to_dict()
# create an instance of PhpIni from a dict
php_ini_from_dict = PhpIni.from_dict(php_ini_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


