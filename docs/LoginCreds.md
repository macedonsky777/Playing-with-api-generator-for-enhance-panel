# LoginCreds


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** |  | 
**password** | **str** |  | 
**device_id** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.login_creds import LoginCreds

# TODO update the JSON string below
json = "{}"
# create an instance of LoginCreds from a JSON string
login_creds_instance = LoginCreds.from_json(json)
# print the JSON string representation of the object
print(LoginCreds.to_json())

# convert the object into a dict
login_creds_dict = login_creds_instance.to_dict()
# create an instance of LoginCreds from a dict
login_creds_from_dict = LoginCreds.from_dict(login_creds_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


