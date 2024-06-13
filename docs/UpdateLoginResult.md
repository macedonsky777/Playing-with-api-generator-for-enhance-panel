# UpdateLoginResult


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**otp_url** | **str** |  | [optional] 
**verify_pin** | **bool** |  | [optional] 

## Example

```python
from openapi_client.models.update_login_result import UpdateLoginResult

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateLoginResult from a JSON string
update_login_result_instance = UpdateLoginResult.from_json(json)
# print the JSON string representation of the object
print(UpdateLoginResult.to_json())

# convert the object into a dict
update_login_result_dict = update_login_result_instance.to_dict()
# create an instance of UpdateLoginResult from a dict
update_login_result_from_dict = UpdateLoginResult.from_dict(update_login_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


