# CoreServiceInfo


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
from openapi_client.models.core_service_info import CoreServiceInfo

# TODO update the JSON string below
json = "{}"
# create an instance of CoreServiceInfo from a JSON string
core_service_info_instance = CoreServiceInfo.from_json(json)
# print the JSON string representation of the object
print(CoreServiceInfo.to_json())

# convert the object into a dict
core_service_info_dict = core_service_info_instance.to_dict()
# create an instance of CoreServiceInfo from a dict
core_service_info_from_dict = CoreServiceInfo.from_dict(core_service_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


