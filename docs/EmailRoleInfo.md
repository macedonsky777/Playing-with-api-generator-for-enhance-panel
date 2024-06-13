# EmailRoleInfo


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**state** | [**ServerRoleState**](ServerRoleState.md) |  | 
**usage** | **int** |  | 
**mailbox_count** | **int** |  | 
**failed_delivery_count** | **int** |  | 
**mtacd** | [**ServiceInfo**](ServiceInfo.md) |  | 
**imapcd** | [**ServiceInfo**](ServiceInfo.md) |  | 
**spamcd** | [**ServiceInfo**](ServiceInfo.md) |  | 
**websites_count** | **int** | The number of websites whose emails are assigned to be on this email role. | 

## Example

```python
from openapi_client.models.email_role_info import EmailRoleInfo

# TODO update the JSON string below
json = "{}"
# create an instance of EmailRoleInfo from a JSON string
email_role_info_instance = EmailRoleInfo.from_json(json)
# print the JSON string representation of the object
print(EmailRoleInfo.to_json())

# convert the object into a dict
email_role_info_dict = email_role_info_instance.to_dict()
# create an instance of EmailRoleInfo from a dict
email_role_info_from_dict = EmailRoleInfo.from_dict(email_role_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


