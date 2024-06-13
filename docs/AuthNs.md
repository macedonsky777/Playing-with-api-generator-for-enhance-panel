# AuthNs

Authoritative Name Server

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ip** | **str** | Server IP address | [optional] 
**domain_ips** | **List[str]** | list of resolved ip addresses for the domain | [optional] 
**delegations** | [**Dict[str, AuthNs]**](AuthNs.md) | Tree of delegated AuthNs servers | [optional] 

## Example

```python
from openapi_client.models.auth_ns import AuthNs

# TODO update the JSON string below
json = "{}"
# create an instance of AuthNs from a JSON string
auth_ns_instance = AuthNs.from_json(json)
# print the JSON string representation of the object
print(AuthNs.to_json())

# convert the object into a dict
auth_ns_dict = auth_ns_instance.to_dict()
# create an instance of AuthNs from a dict
auth_ns_from_dict = AuthNs.from_dict(auth_ns_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


