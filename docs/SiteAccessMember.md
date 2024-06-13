# SiteAccessMember


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**name** | **str** |  | 
**email** | **str** |  | 
**avatar_path** | **str** |  | [optional] 
**color_code** | **str** |  | 

## Example

```python
from openapi_client.models.site_access_member import SiteAccessMember

# TODO update the JSON string below
json = "{}"
# create an instance of SiteAccessMember from a JSON string
site_access_member_instance = SiteAccessMember.from_json(json)
# print the JSON string representation of the object
print(SiteAccessMember.to_json())

# convert the object into a dict
site_access_member_dict = site_access_member_instance.to_dict()
# create an instance of SiteAccessMember from a dict
site_access_member_from_dict = SiteAccessMember.from_dict(site_access_member_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


