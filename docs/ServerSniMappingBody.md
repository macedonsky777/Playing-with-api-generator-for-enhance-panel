# ServerSniMappingBody


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cert_id** | **str** |  | 
**hostname** | **str** |  | 

## Example

```python
from openapi_client.models.server_sni_mapping_body import ServerSniMappingBody

# TODO update the JSON string below
json = "{}"
# create an instance of ServerSniMappingBody from a JSON string
server_sni_mapping_body_instance = ServerSniMappingBody.from_json(json)
# print the JSON string representation of the object
print(ServerSniMappingBody.to_json())

# convert the object into a dict
server_sni_mapping_body_dict = server_sni_mapping_body_instance.to_dict()
# create an instance of ServerSniMappingBody from a dict
server_sni_mapping_body_from_dict = ServerSniMappingBody.from_dict(server_sni_mapping_body_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


