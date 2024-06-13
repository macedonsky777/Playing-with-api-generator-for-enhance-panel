# InviteValidation


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**is_valid** | **bool** |  | 
**login_id** | **str** |  | [optional] 
**org_id** | **str** |  | [optional] 
**org_name** | **str** |  | [optional] 
**role** | [**Role**](Role.md) |  | [optional] 

## Example

```python
from openapi_client.models.invite_validation import InviteValidation

# TODO update the JSON string below
json = "{}"
# create an instance of InviteValidation from a JSON string
invite_validation_instance = InviteValidation.from_json(json)
# print the JSON string representation of the object
print(InviteValidation.to_json())

# convert the object into a dict
invite_validation_dict = invite_validation_instance.to_dict()
# create an instance of InviteValidation from a dict
invite_validation_from_dict = InviteValidation.from_dict(invite_validation_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


