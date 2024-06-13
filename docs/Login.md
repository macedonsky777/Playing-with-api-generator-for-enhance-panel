# Login


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**email** | **str** |  | 
**name** | **str** |  | 
**color_code** | **str** |  | 
**registered_at** | **str** |  | 
**avatar_path** | **str** |  | [optional] 
**password_last_changed_at** | **str** |  | [optional] 
**auth_method** | **str** |  | 
**locale** | [**CPLocale**](CPLocale.md) |  | 

## Example

```python
from openapi_client.models.login import Login

# TODO update the JSON string below
json = "{}"
# create an instance of Login from a JSON string
login_instance = Login.from_json(json)
# print the JSON string representation of the object
print(Login.to_json())

# convert the object into a dict
login_dict = login_instance.to_dict()
# create an instance of Login from a dict
login_from_dict = Login.from_dict(login_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


