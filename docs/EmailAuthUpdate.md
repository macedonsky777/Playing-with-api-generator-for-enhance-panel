# EmailAuthUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**dkim** | **bool** |  | [optional] 

## Example

```python
from openapi_client.models.email_auth_update import EmailAuthUpdate

# TODO update the JSON string below
json = "{}"
# create an instance of EmailAuthUpdate from a JSON string
email_auth_update_instance = EmailAuthUpdate.from_json(json)
# print the JSON string representation of the object
print(EmailAuthUpdate.to_json())

# convert the object into a dict
email_auth_update_dict = email_auth_update_instance.to_dict()
# create an instance of EmailAuthUpdate from a dict
email_auth_update_from_dict = EmailAuthUpdate.from_dict(email_auth_update_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


