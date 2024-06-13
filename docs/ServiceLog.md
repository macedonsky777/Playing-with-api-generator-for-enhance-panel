# ServiceLog


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_at** | **date** |  | 
**service_kind** | [**DaemonKind**](DaemonKind.md) |  | 
**status** | [**ServiceLogStatus**](ServiceLogStatus.md) |  | 
**metadata** | [**ServiceLogMetadata**](ServiceLogMetadata.md) |  | [optional] 

## Example

```python
from openapi_client.models.service_log import ServiceLog

# TODO update the JSON string below
json = "{}"
# create an instance of ServiceLog from a JSON string
service_log_instance = ServiceLog.from_json(json)
# print the JSON string representation of the object
print(ServiceLog.to_json())

# convert the object into a dict
service_log_dict = service_log_instance.to_dict()
# create an instance of ServiceLog from a dict
service_log_from_dict = ServiceLog.from_dict(service_log_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


