# Member


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**login_id** | **str** |  | 
**is_active** | **bool** |  | 
**email** | **str** |  | 
**name** | **str** |  | 
**roles** | [**List[Role]**](Role.md) |  | 
**site_accesses** | **List[str]** | This field is only present if member has \&quot;SiteAccess\&quot; role. In this case, the list contains the ids of the websites to which member has access. | 
**notifications** | **List[str]** | The notifications configured for this member. | 
**joined_at** | **date** |  | 
**avatar_path** | **str** |  | [optional] 
**color_code** | **str** |  | 

## Example

```python
from openapi_client.models.member import Member

# TODO update the JSON string below
json = "{}"
# create an instance of Member from a JSON string
member_instance = Member.from_json(json)
# print the JSON string representation of the object
print(Member.to_json())

# convert the object into a dict
member_dict = member_instance.to_dict()
# create an instance of Member from a dict
member_from_dict = Member.from_dict(member_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


