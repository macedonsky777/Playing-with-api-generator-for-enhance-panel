# NewMember


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**login_id** | **str** |  | 
**roles** | [**List[Role]**](Role.md) |  | 

## Example

```python
from openapi_client.models.new_member import NewMember

# TODO update the JSON string below
json = "{}"
# create an instance of NewMember from a JSON string
new_member_instance = NewMember.from_json(json)
# print the JSON string representation of the object
print(NewMember.to_json())

# convert the object into a dict
new_member_dict = new_member_instance.to_dict()
# create an instance of NewMember from a dict
new_member_from_dict = NewMember.from_dict(new_member_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


