# ServerConf


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**friendly_name** | **str** |  | [optional] 
**group** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.server_conf import ServerConf

# TODO update the JSON string below
json = "{}"
# create an instance of ServerConf from a JSON string
server_conf_instance = ServerConf.from_json(json)
# print the JSON string representation of the object
print(ServerConf.to_json())

# convert the object into a dict
server_conf_dict = server_conf_instance.to_dict()
# create an instance of ServerConf from a dict
server_conf_from_dict = ServerConf.from_dict(server_conf_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


