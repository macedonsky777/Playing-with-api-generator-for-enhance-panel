# EmailAuthValidation


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**dkim_is_valid** | **bool** |  | 
**spf_is_valid** | **bool** |  | 
**found_txt_records_dkim** | **List[str]** |  | 
**found_txt_records_spf** | **List[str]** |  | [optional] 

## Example

```python
from openapi_client.models.email_auth_validation import EmailAuthValidation

# TODO update the JSON string below
json = "{}"
# create an instance of EmailAuthValidation from a JSON string
email_auth_validation_instance = EmailAuthValidation.from_json(json)
# print the JSON string representation of the object
print(EmailAuthValidation.to_json())

# convert the object into a dict
email_auth_validation_dict = email_auth_validation_instance.to_dict()
# create an instance of EmailAuthValidation from a dict
email_auth_validation_from_dict = EmailAuthValidation.from_dict(email_auth_validation_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


