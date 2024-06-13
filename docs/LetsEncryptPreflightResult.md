# LetsEncryptPreflightResult


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**can_issue** | **bool** |  | 
**error** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.lets_encrypt_preflight_result import LetsEncryptPreflightResult

# TODO update the JSON string below
json = "{}"
# create an instance of LetsEncryptPreflightResult from a JSON string
lets_encrypt_preflight_result_instance = LetsEncryptPreflightResult.from_json(json)
# print the JSON string representation of the object
print(LetsEncryptPreflightResult.to_json())

# convert the object into a dict
lets_encrypt_preflight_result_dict = lets_encrypt_preflight_result_instance.to_dict()
# create an instance of LetsEncryptPreflightResult from a dict
lets_encrypt_preflight_result_from_dict = LetsEncryptPreflightResult.from_dict(lets_encrypt_preflight_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


