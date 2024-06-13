# WebsiteOperationValidation


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**operation** | [**WebsiteOperation**](WebsiteOperation.md) |  | 
**params** | [**ChangeSubscriptionParams**](ChangeSubscriptionParams.md) |  | [optional] 

## Example

```python
from openapi_client.models.website_operation_validation import WebsiteOperationValidation

# TODO update the JSON string below
json = "{}"
# create an instance of WebsiteOperationValidation from a JSON string
website_operation_validation_instance = WebsiteOperationValidation.from_json(json)
# print the JSON string representation of the object
print(WebsiteOperationValidation.to_json())

# convert the object into a dict
website_operation_validation_dict = website_operation_validation_instance.to_dict()
# create an instance of WebsiteOperationValidation from a dict
website_operation_validation_from_dict = WebsiteOperationValidation.from_dict(website_operation_validation_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


