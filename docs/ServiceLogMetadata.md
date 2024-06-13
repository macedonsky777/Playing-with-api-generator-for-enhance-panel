# ServiceLogMetadata


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**request_time_ms** | **int** |  | 
**greetings_message** | **str** | This is a list of bytes which have been returned by the service. For example \&quot;[50,50,48,32]\&quot;. | 

## Example

```python
from openapi_client.models.service_log_metadata import ServiceLogMetadata

# TODO update the JSON string below
json = "{}"
# create an instance of ServiceLogMetadata from a JSON string
service_log_metadata_instance = ServiceLogMetadata.from_json(json)
# print the JSON string representation of the object
print(ServiceLogMetadata.to_json())

# convert the object into a dict
service_log_metadata_dict = service_log_metadata_instance.to_dict()
# create an instance of ServiceLogMetadata from a dict
service_log_metadata_from_dict = ServiceLogMetadata.from_dict(service_log_metadata_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


