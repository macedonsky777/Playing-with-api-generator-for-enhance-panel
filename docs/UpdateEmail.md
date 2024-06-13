# UpdateEmail


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**mailbox_name** | **str** |  | [optional] 
**mailbox_password** | **str** |  | [optional] 
**aliases** | **List[str]** |  | [optional] 
**forwarders** | **List[str]** |  | [optional] 
**has_mailbox** | **bool** |  | [optional] 
**status** | [**EmailStatus**](EmailStatus.md) |  | [optional] 
**quota** | **int** |  | [optional] 
**spam_threshold** | **int** |  | [optional] 
**spam_delivery** | **str** |  | [optional] 
**blacklist** | **List[str]** |  | [optional] 
**whitelist** | **List[str]** |  | [optional] 

## Example

```python
from openapi_client.models.update_email import UpdateEmail

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateEmail from a JSON string
update_email_instance = UpdateEmail.from_json(json)
# print the JSON string representation of the object
print(UpdateEmail.to_json())

# convert the object into a dict
update_email_dict = update_email_instance.to_dict()
# create an instance of UpdateEmail from a dict
update_email_from_dict = UpdateEmail.from_dict(update_email_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


