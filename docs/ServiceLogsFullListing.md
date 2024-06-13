# ServiceLogsFullListing


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[ServiceLog]**](ServiceLog.md) |  | 

## Example

```python
from openapi_client.models.service_logs_full_listing import ServiceLogsFullListing

# TODO update the JSON string below
json = "{}"
# create an instance of ServiceLogsFullListing from a JSON string
service_logs_full_listing_instance = ServiceLogsFullListing.from_json(json)
# print the JSON string representation of the object
print(ServiceLogsFullListing.to_json())

# convert the object into a dict
service_logs_full_listing_dict = service_logs_full_listing_instance.to_dict()
# create an instance of ServiceLogsFullListing from a dict
service_logs_full_listing_from_dict = ServiceLogsFullListing.from_dict(service_logs_full_listing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


