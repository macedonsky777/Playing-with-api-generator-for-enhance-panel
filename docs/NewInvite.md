# NewInvite


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** |  | 
**name** | **str** |  | 
**roles** | [**List[Role]**](Role.md) |  | 
**site_accesses** | **List[str]** |  | [optional] 
**notifications** | **List[str]** |  | [optional] 
**send_email** | **bool** | Whether to send an email to the invitee. Defaults to true if not provided. | [optional] 

## Example

```python
from openapi_client.models.new_invite import NewInvite

# TODO update the JSON string below
json = "{}"
# create an instance of NewInvite from a JSON string
new_invite_instance = NewInvite.from_json(json)
# print the JSON string representation of the object
print(NewInvite.to_json())

# convert the object into a dict
new_invite_dict = new_invite_instance.to_dict()
# create an instance of NewInvite from a dict
new_invite_from_dict = NewInvite.from_dict(new_invite_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


