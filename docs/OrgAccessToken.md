# OrgAccessToken


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**first_five** | **str** |  | 
**roles** | [**List[Role]**](Role.md) |  | 
**token_expires** | **str** |  | [optional] 
**friendly_name** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.org_access_token import OrgAccessToken

# TODO update the JSON string below
json = "{}"
# create an instance of OrgAccessToken from a JSON string
org_access_token_instance = OrgAccessToken.from_json(json)
# print the JSON string representation of the object
print(OrgAccessToken.to_json())

# convert the object into a dict
org_access_token_dict = org_access_token_instance.to_dict()
# create an instance of OrgAccessToken from a dict
org_access_token_from_dict = OrgAccessToken.from_dict(org_access_token_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


