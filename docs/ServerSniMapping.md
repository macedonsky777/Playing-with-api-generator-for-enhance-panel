# ServerSniMapping


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**server_id** | **str** |  | 
**cert_id** | **str** |  | 
**hostname** | **str** |  | 

## Example

```python
from openapi_client.models.server_sni_mapping import ServerSniMapping

# TODO update the JSON string below
json = "{}"
# create an instance of ServerSniMapping from a JSON string
server_sni_mapping_instance = ServerSniMapping.from_json(json)
# print the JSON string representation of the object
print(ServerSniMapping.to_json())

# convert the object into a dict
server_sni_mapping_dict = server_sni_mapping_instance.to_dict()
# create an instance of ServerSniMapping from a dict
server_sni_mapping_from_dict = ServerSniMapping.from_dict(server_sni_mapping_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


