# LogTimeMetadata

How long the request took. It's used with `ok` and `slow` log statuses.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**request_time_ms** | **int** |  | 

## Example

```python
from openapi_client.models.log_time_metadata import LogTimeMetadata

# TODO update the JSON string below
json = "{}"
# create an instance of LogTimeMetadata from a JSON string
log_time_metadata_instance = LogTimeMetadata.from_json(json)
# print the JSON string representation of the object
print(LogTimeMetadata.to_json())

# convert the object into a dict
log_time_metadata_dict = log_time_metadata_instance.to_dict()
# create an instance of LogTimeMetadata from a dict
log_time_metadata_from_dict = LogTimeMetadata.from_dict(log_time_metadata_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


