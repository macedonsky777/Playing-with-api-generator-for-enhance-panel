# DockerRegistry


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** |  | 
**user** | **str** |  | 
**password** | **str** |  | 

## Example

```python
from openapi_client.models.docker_registry import DockerRegistry

# TODO update the JSON string below
json = "{}"
# create an instance of DockerRegistry from a JSON string
docker_registry_instance = DockerRegistry.from_json(json)
# print the JSON string representation of the object
print(DockerRegistry.to_json())

# convert the object into a dict
docker_registry_dict = docker_registry_instance.to_dict()
# create an instance of DockerRegistry from a dict
docker_registry_from_dict = DockerRegistry.from_dict(docker_registry_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


