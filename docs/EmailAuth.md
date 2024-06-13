# EmailAuth


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**dkim** | **bool** |  | 
**dkim_public_key** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.email_auth import EmailAuth

# TODO update the JSON string below
json = "{}"
# create an instance of EmailAuth from a JSON string
email_auth_instance = EmailAuth.from_json(json)
# print the JSON string representation of the object
print(EmailAuth.to_json())

# convert the object into a dict
email_auth_dict = email_auth_instance.to_dict()
# create an instance of EmailAuth from a dict
email_auth_from_dict = EmailAuth.from_dict(email_auth_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


