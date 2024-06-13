# WpUser


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**login** | **str** |  | 
**email** | **str** |  | 

## Example

```python
from openapi_client.models.wp_user import WpUser

# TODO update the JSON string below
json = "{}"
# create an instance of WpUser from a JSON string
wp_user_instance = WpUser.from_json(json)
# print the JSON string representation of the object
print(WpUser.to_json())

# convert the object into a dict
wp_user_dict = wp_user_instance.to_dict()
# create an instance of WpUser from a dict
wp_user_from_dict = WpUser.from_dict(wp_user_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


