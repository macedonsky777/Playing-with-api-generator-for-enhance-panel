# NewAccessToken


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**roles** | [**List[Role]**](Role.md) |  | 
**token_expires** | **datetime** |  | [optional] 
**friendly_name** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.new_access_token import NewAccessToken

# TODO update the JSON string below
json = "{}"
# create an instance of NewAccessToken from a JSON string
new_access_token_instance = NewAccessToken.from_json(json)
# print the JSON string representation of the object
print(NewAccessToken.to_json())

# convert the object into a dict
new_access_token_dict = new_access_token_instance.to_dict()
# create an instance of NewAccessToken from a dict
new_access_token_from_dict = NewAccessToken.from_dict(new_access_token_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


