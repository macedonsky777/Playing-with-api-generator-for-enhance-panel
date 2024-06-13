# EmailForwardersUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**forwarders** | **List[str]** | email addresses to forward to. | 

## Example

```python
from openapi_client.models.email_forwarders_update import EmailForwardersUpdate

# TODO update the JSON string below
json = "{}"
# create an instance of EmailForwardersUpdate from a JSON string
email_forwarders_update_instance = EmailForwardersUpdate.from_json(json)
# print the JSON string representation of the object
print(EmailForwardersUpdate.to_json())

# convert the object into a dict
email_forwarders_update_dict = email_forwarders_update_instance.to_dict()
# create an instance of EmailForwardersUpdate from a dict
email_forwarders_update_from_dict = EmailForwardersUpdate.from_dict(email_forwarders_update_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


