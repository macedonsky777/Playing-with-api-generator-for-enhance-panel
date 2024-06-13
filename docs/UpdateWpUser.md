# UpdateWpUser


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**password** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**email** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.update_wp_user import UpdateWpUser

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateWpUser from a JSON string
update_wp_user_instance = UpdateWpUser.from_json(json)
# print the JSON string representation of the object
print(UpdateWpUser.to_json())

# convert the object into a dict
update_wp_user_dict = update_wp_user_instance.to_dict()
# create an instance of UpdateWpUser from a dict
update_wp_user_from_dict = UpdateWpUser.from_dict(update_wp_user_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


