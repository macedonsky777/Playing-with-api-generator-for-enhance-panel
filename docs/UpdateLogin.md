# UpdateLogin


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**email** | **str** |  | [optional] 
**password** | **str** |  | [optional] 
**locale** | [**CPLocale**](CPLocale.md) |  | [optional] 
**auth_method** | **str** |  | [optional] 
**current_password** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.update_login import UpdateLogin

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateLogin from a JSON string
update_login_instance = UpdateLogin.from_json(json)
# print the JSON string representation of the object
print(UpdateLogin.to_json())

# convert the object into a dict
update_login_dict = update_login_instance.to_dict()
# create an instance of UpdateLogin from a dict
update_login_from_dict = UpdateLogin.from_dict(update_login_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


