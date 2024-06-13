# Login2FA


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**auth_method** | **str** |  | 
**pin** | **str** |  | 
**remember_me** | [**Login2FARememberMe**](Login2FARememberMe.md) |  | [optional] 

## Example

```python
from openapi_client.models.login2_fa import Login2FA

# TODO update the JSON string below
json = "{}"
# create an instance of Login2FA from a JSON string
login2_fa_instance = Login2FA.from_json(json)
# print the JSON string representation of the object
print(Login2FA.to_json())

# convert the object into a dict
login2_fa_dict = login2_fa_instance.to_dict()
# create an instance of Login2FA from a dict
login2_fa_from_dict = Login2FA.from_dict(login2_fa_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


