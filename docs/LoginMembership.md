# LoginMembership


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**member_id** | **str** |  | 
**org_id** | **str** |  | 
**org_name** | **str** |  | 
**is_master_org** | **bool** |  | 
**roles** | [**List[Role]**](Role.md) |  | 
**site_access_count** | **float** |  | 

## Example

```python
from openapi_client.models.login_membership import LoginMembership

# TODO update the JSON string below
json = "{}"
# create an instance of LoginMembership from a JSON string
login_membership_instance = LoginMembership.from_json(json)
# print the JSON string representation of the object
print(LoginMembership.to_json())

# convert the object into a dict
login_membership_dict = login_membership_instance.to_dict()
# create an instance of LoginMembership from a dict
login_membership_from_dict = LoginMembership.from_dict(login_membership_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


