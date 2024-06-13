# SetWebserverKind


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**webserver_kind** | [**WebserverKind**](WebserverKind.md) |  | 
**serial** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.set_webserver_kind import SetWebserverKind

# TODO update the JSON string below
json = "{}"
# create an instance of SetWebserverKind from a JSON string
set_webserver_kind_instance = SetWebserverKind.from_json(json)
# print the JSON string representation of the object
print(SetWebserverKind.to_json())

# convert the object into a dict
set_webserver_kind_dict = set_webserver_kind_instance.to_dict()
# create an instance of SetWebserverKind from a dict
set_webserver_kind_from_dict = SetWebserverKind.from_dict(set_webserver_kind_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


