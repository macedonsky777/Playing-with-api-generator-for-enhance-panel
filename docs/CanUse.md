# CanUse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ftp** | **bool** |  | 
**file_manager** | **bool** |  | 
**php_versions** | [**List[PhpVersion]**](PhpVersion.md) |  | 
**redis** | **bool** |  | 
**mod_sec** | **bool** |  | 
**backup** | **bool** |  | 
**mysql_kind** | [**MysqlKind**](MysqlKind.md) |  | [optional] 

## Example

```python
from openapi_client.models.can_use import CanUse

# TODO update the JSON string below
json = "{}"
# create an instance of CanUse from a JSON string
can_use_instance = CanUse.from_json(json)
# print the JSON string representation of the object
print(CanUse.to_json())

# convert the object into a dict
can_use_dict = can_use_instance.to_dict()
# create an instance of CanUse from a dict
can_use_from_dict = CanUse.from_dict(can_use_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


