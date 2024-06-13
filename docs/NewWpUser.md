# NewWpUser


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**login** | **str** |  | 
**name** | **str** |  | [optional] 
**password** | **str** |  | 
**email** | **str** |  | 

## Example

```python
from openapi_client.models.new_wp_user import NewWpUser

# TODO update the JSON string below
json = "{}"
# create an instance of NewWpUser from a JSON string
new_wp_user_instance = NewWpUser.from_json(json)
# print the JSON string representation of the object
print(NewWpUser.to_json())

# convert the object into a dict
new_wp_user_dict = new_wp_user_instance.to_dict()
# create an instance of NewWpUser from a dict
new_wp_user_from_dict = NewWpUser.from_dict(new_wp_user_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


