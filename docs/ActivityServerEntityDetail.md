# ActivityServerEntityDetail


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**friendly_name** | **str** |  | 
**hostname** | **str** |  | 

## Example

```python
from openapi_client.models.activity_server_entity_detail import ActivityServerEntityDetail

# TODO update the JSON string below
json = "{}"
# create an instance of ActivityServerEntityDetail from a JSON string
activity_server_entity_detail_instance = ActivityServerEntityDetail.from_json(json)
# print the JSON string representation of the object
print(ActivityServerEntityDetail.to_json())

# convert the object into a dict
activity_server_entity_detail_dict = activity_server_entity_detail_instance.to_dict()
# create an instance of ActivityServerEntityDetail from a dict
activity_server_entity_detail_from_dict = ActivityServerEntityDetail.from_dict(activity_server_entity_detail_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


