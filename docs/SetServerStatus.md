# SetServerStatus


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**action** | [**ServerStatusAction**](ServerStatusAction.md) |  | 

## Example

```python
from openapi_client.models.set_server_status import SetServerStatus

# TODO update the JSON string below
json = "{}"
# create an instance of SetServerStatus from a JSON string
set_server_status_instance = SetServerStatus.from_json(json)
# print the JSON string representation of the object
print(SetServerStatus.to_json())

# convert the object into a dict
set_server_status_dict = set_server_status_instance.to_dict()
# create an instance of SetServerStatus from a dict
set_server_status_from_dict = SetServerStatus.from_dict(set_server_status_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


