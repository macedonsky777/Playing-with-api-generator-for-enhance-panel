# WebsiteLog


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_at** | **date** |  | 
**status** | [**WebsiteLogStatus**](WebsiteLogStatus.md) |  | 
**metadata** | [**WebsiteLogMetadata**](WebsiteLogMetadata.md) |  | [optional] 

## Example

```python
from openapi_client.models.website_log import WebsiteLog

# TODO update the JSON string below
json = "{}"
# create an instance of WebsiteLog from a JSON string
website_log_instance = WebsiteLog.from_json(json)
# print the JSON string representation of the object
print(WebsiteLog.to_json())

# convert the object into a dict
website_log_dict = website_log_instance.to_dict()
# create an instance of WebsiteLog from a dict
website_log_from_dict = WebsiteLog.from_dict(website_log_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


