# AcceptInviteBody


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** |  | 
**password** | **str** |  | [optional] 
**locale** | [**CPLocale**](CPLocale.md) |  | [optional] 

## Example

```python
from openapi_client.models.accept_invite_body import AcceptInviteBody

# TODO update the JSON string below
json = "{}"
# create an instance of AcceptInviteBody from a JSON string
accept_invite_body_instance = AcceptInviteBody.from_json(json)
# print the JSON string representation of the object
print(AcceptInviteBody.to_json())

# convert the object into a dict
accept_invite_body_dict = accept_invite_body_instance.to_dict()
# create an instance of AcceptInviteBody from a dict
accept_invite_body_from_dict = AcceptInviteBody.from_dict(accept_invite_body_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


