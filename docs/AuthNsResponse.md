# AuthNsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**matches_platform** | **bool** |  | 
**auth_ns** | [**List[AuthNsResponseNs]**](AuthNsResponseNs.md) |  | 

## Example

```python
from openapi_client.models.auth_ns_response import AuthNsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AuthNsResponse from a JSON string
auth_ns_response_instance = AuthNsResponse.from_json(json)
# print the JSON string representation of the object
print(AuthNsResponse.to_json())

# convert the object into a dict
auth_ns_response_dict = auth_ns_response_instance.to_dict()
# create an instance of AuthNsResponse from a dict
auth_ns_response_from_dict = AuthNsResponse.from_dict(auth_ns_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


