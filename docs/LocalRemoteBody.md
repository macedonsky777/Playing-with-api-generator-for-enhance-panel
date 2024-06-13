# LocalRemoteBody

Whether a domain is treated as local or remote by the MTA

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**local_remote** | [**LocalRemote**](LocalRemote.md) |  | [optional] 

## Example

```python
from openapi_client.models.local_remote_body import LocalRemoteBody

# TODO update the JSON string below
json = "{}"
# create an instance of LocalRemoteBody from a JSON string
local_remote_body_instance = LocalRemoteBody.from_json(json)
# print the JSON string representation of the object
print(LocalRemoteBody.to_json())

# convert the object into a dict
local_remote_body_dict = local_remote_body_instance.to_dict()
# create an instance of LocalRemoteBody from a dict
local_remote_body_from_dict = LocalRemoteBody.from_dict(local_remote_body_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


