# SetServiceStatus


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**action** | [**ServiceStatusAction**](ServiceStatusAction.md) |  | 

## Example

```python
from openapi_client.models.set_service_status import SetServiceStatus

# TODO update the JSON string below
json = "{}"
# create an instance of SetServiceStatus from a JSON string
set_service_status_instance = SetServiceStatus.from_json(json)
# print the JSON string representation of the object
print(SetServiceStatus.to_json())

# convert the object into a dict
set_service_status_dict = set_service_status_instance.to_dict()
# create an instance of SetServiceStatus from a dict
set_service_status_from_dict = SetServiceStatus.from_dict(set_service_status_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


