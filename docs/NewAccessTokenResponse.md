# NewAccessTokenResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**first_five** | **str** |  | 
**unencrypted_token** | **str** |  | 

## Example

```python
from openapi_client.models.new_access_token_response import NewAccessTokenResponse

# TODO update the JSON string below
json = "{}"
# create an instance of NewAccessTokenResponse from a JSON string
new_access_token_response_instance = NewAccessTokenResponse.from_json(json)
# print the JSON string representation of the object
print(NewAccessTokenResponse.to_json())

# convert the object into a dict
new_access_token_response_dict = new_access_token_response_instance.to_dict()
# create an instance of NewAccessTokenResponse from a dict
new_access_token_response_from_dict = NewAccessTokenResponse.from_dict(new_access_token_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


