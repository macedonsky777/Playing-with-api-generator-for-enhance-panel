# InterfaceIp


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ip** | **str** |  | 
**prefix** | **str** |  | 
**kind** | **str** |  | 

## Example

```python
from openapi_client.models.interface_ip import InterfaceIp

# TODO update the JSON string below
json = "{}"
# create an instance of InterfaceIp from a JSON string
interface_ip_instance = InterfaceIp.from_json(json)
# print the JSON string representation of the object
print(InterfaceIp.to_json())

# convert the object into a dict
interface_ip_dict = interface_ip_instance.to_dict()
# create an instance of InterfaceIp from a dict
interface_ip_from_dict = InterfaceIp.from_dict(interface_ip_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


