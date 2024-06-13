# ServiceInfo


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**version** | **str** |  | [optional] 
**status** | [**NetworkStatus**](NetworkStatus.md) |  | 
**port** | **int** |  | 
**usage** | **int** |  | 
**processes** | [**List[ProcessInfo]**](ProcessInfo.md) |  | [optional] 

## Example

```python
from openapi_client.models.service_info import ServiceInfo

# TODO update the JSON string below
json = "{}"
# create an instance of ServiceInfo from a JSON string
service_info_instance = ServiceInfo.from_json(json)
# print the JSON string representation of the object
print(ServiceInfo.to_json())

# convert the object into a dict
service_info_dict = service_info_instance.to_dict()
# create an instance of ServiceInfo from a dict
service_info_from_dict = ServiceInfo.from_dict(service_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


