# LogHttpMetadata

What was the status code of an http request and its truncated body. Used with `failed4xx` and `failed5xx` statuses.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status_code** | **int** |  | 
**body** | **str** |  | 

## Example

```python
from openapi_client.models.log_http_metadata import LogHttpMetadata

# TODO update the JSON string below
json = "{}"
# create an instance of LogHttpMetadata from a JSON string
log_http_metadata_instance = LogHttpMetadata.from_json(json)
# print the JSON string representation of the object
print(LogHttpMetadata.to_json())

# convert the object into a dict
log_http_metadata_dict = log_http_metadata_instance.to_dict()
# create an instance of LogHttpMetadata from a dict
log_http_metadata_from_dict = LogHttpMetadata.from_dict(log_http_metadata_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


