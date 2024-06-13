# Login2FARememberMe


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**device_id** | **str** | The unique ID of the device. It has to be 32 character; | 
**ttl** | **int** | Defines how many seconds deviceId will be remembered. Min 1 hour, max 3 months | 

## Example

```python
from openapi_client.models.login2_fa_remember_me import Login2FARememberMe

# TODO update the JSON string below
json = "{}"
# create an instance of Login2FARememberMe from a JSON string
login2_fa_remember_me_instance = Login2FARememberMe.from_json(json)
# print the JSON string representation of the object
print(Login2FARememberMe.to_json())

# convert the object into a dict
login2_fa_remember_me_dict = login2_fa_remember_me_instance.to_dict()
# create an instance of Login2FARememberMe from a dict
login2_fa_remember_me_from_dict = Login2FARememberMe.from_dict(login2_fa_remember_me_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


