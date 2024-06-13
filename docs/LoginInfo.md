# LoginInfo


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** |  | 
**password** | **str** |  | 
**name** | **str** |  | 

## Example

```python
from openapi_client.models.login_info import LoginInfo

# TODO update the JSON string below
json = "{}"
# create an instance of LoginInfo from a JSON string
login_info_instance = LoginInfo.from_json(json)
# print the JSON string representation of the object
print(LoginInfo.to_json())

# convert the object into a dict
login_info_dict = login_info_instance.to_dict()
# create an instance of LoginInfo from a dict
login_info_from_dict = LoginInfo.from_dict(login_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


