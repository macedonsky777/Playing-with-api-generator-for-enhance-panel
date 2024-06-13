# LoginMemberships


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**memberships** | [**List[LoginMembership]**](LoginMembership.md) |  | 

## Example

```python
from openapi_client.models.login_memberships import LoginMemberships

# TODO update the JSON string below
json = "{}"
# create an instance of LoginMemberships from a JSON string
login_memberships_instance = LoginMemberships.from_json(json)
# print the JSON string representation of the object
print(LoginMemberships.to_json())

# convert the object into a dict
login_memberships_dict = login_memberships_instance.to_dict()
# create an instance of LoginMemberships from a dict
login_memberships_from_dict = LoginMemberships.from_dict(login_memberships_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


