# SetupResult


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**login_id** | **str** |  | 
**member_id** | **str** |  | 
**org_id** | **str** |  | 
**server_id** | **str** |  | 
**control_panel_website_id** | **str** |  | 

## Example

```python
from openapi_client.models.setup_result import SetupResult

# TODO update the JSON string below
json = "{}"
# create an instance of SetupResult from a JSON string
setup_result_instance = SetupResult.from_json(json)
# print the JSON string representation of the object
print(SetupResult.to_json())

# convert the object into a dict
setup_result_dict = setup_result_instance.to_dict()
# create an instance of SetupResult from a dict
setup_result_from_dict = SetupResult.from_dict(setup_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


