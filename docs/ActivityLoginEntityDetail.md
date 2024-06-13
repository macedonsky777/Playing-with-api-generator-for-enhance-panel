# ActivityLoginEntityDetail


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**email** | **str** |  | 
**realm_id** | **str** |  | 

## Example

```python
from openapi_client.models.activity_login_entity_detail import ActivityLoginEntityDetail

# TODO update the JSON string below
json = "{}"
# create an instance of ActivityLoginEntityDetail from a JSON string
activity_login_entity_detail_instance = ActivityLoginEntityDetail.from_json(json)
# print the JSON string representation of the object
print(ActivityLoginEntityDetail.to_json())

# convert the object into a dict
activity_login_entity_detail_dict = activity_login_entity_detail_instance.to_dict()
# create an instance of ActivityLoginEntityDetail from a dict
activity_login_entity_detail_from_dict = ActivityLoginEntityDetail.from_dict(activity_login_entity_detail_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


