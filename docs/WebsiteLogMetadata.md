# WebsiteLogMetadata


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**request_time_ms** | **int** |  | 
**status_code** | **int** |  | 
**body** | **str** |  | 

## Example

```python
from openapi_client.models.website_log_metadata import WebsiteLogMetadata

# TODO update the JSON string below
json = "{}"
# create an instance of WebsiteLogMetadata from a JSON string
website_log_metadata_instance = WebsiteLogMetadata.from_json(json)
# print the JSON string representation of the object
print(WebsiteLogMetadata.to_json())

# convert the object into a dict
website_log_metadata_dict = website_log_metadata_instance.to_dict()
# create an instance of WebsiteLogMetadata from a dict
website_log_metadata_from_dict = WebsiteLogMetadata.from_dict(website_log_metadata_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


