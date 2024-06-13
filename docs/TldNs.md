# TldNs

Tree starting from top level DNS and recursively going down to

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ip** | **str** |  | 
**auth_ns_map** | [**Dict[str, AuthNs]**](AuthNs.md) | Tree of AuthNs servers | 

## Example

```python
from openapi_client.models.tld_ns import TldNs

# TODO update the JSON string below
json = "{}"
# create an instance of TldNs from a JSON string
tld_ns_instance = TldNs.from_json(json)
# print the JSON string representation of the object
print(TldNs.to_json())

# convert the object into a dict
tld_ns_dict = tld_ns_instance.to_dict()
# create an instance of TldNs from a dict
tld_ns_from_dict = TldNs.from_dict(tld_ns_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


