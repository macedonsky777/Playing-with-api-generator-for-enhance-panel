# MysqlInfo


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**mysql_kind** | [**MysqlKind**](MysqlKind.md) |  | 

## Example

```python
from openapi_client.models.mysql_info import MysqlInfo

# TODO update the JSON string below
json = "{}"
# create an instance of MysqlInfo from a JSON string
mysql_info_instance = MysqlInfo.from_json(json)
# print the JSON string representation of the object
print(MysqlInfo.to_json())

# convert the object into a dict
mysql_info_dict = mysql_info_instance.to_dict()
# create an instance of MysqlInfo from a dict
mysql_info_from_dict = MysqlInfo.from_dict(mysql_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


