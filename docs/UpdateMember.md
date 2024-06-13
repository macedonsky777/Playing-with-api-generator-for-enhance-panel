# UpdateMember


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**roles** | [**List[Role]**](Role.md) |  | [optional] 
**site_accesses** | **List[str]** | This field is only present if member has \&quot;SiteAccess\&quot; role. In this case, the list contains the ids of the websites to which member has access. | [optional] 
**notifications** | **List[str]** |  | [optional] 

## Example

```python
from openapi_client.models.update_member import UpdateMember

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateMember from a JSON string
update_member_instance = UpdateMember.from_json(json)
# print the JSON string representation of the object
print(UpdateMember.to_json())

# convert the object into a dict
update_member_dict = update_member_instance.to_dict()
# create an instance of UpdateMember from a dict
update_member_from_dict = UpdateMember.from_dict(update_member_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


