# Email


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**website_id** | **str** |  | 
**mailbox_name** | **str** |  | [optional] 
**address** | **str** |  | 
**aliases** | **List[str]** |  | 
**mailbox_id** | **str** |  | [optional] 
**status** | [**EmailStatus**](EmailStatus.md) |  | 
**quota** | [**Quota**](Quota.md) |  | [optional] 
**autoresponders_count** | **int** |  | 
**forwarders_count** | **int** |  | [optional] 
**created_at** | **str** |  | [optional] 
**email_kind** | **str** |  | [optional] 
**domain_id** | **str** |  | 

## Example

```python
from openapi_client.models.email import Email

# TODO update the JSON string below
json = "{}"
# create an instance of Email from a JSON string
email_instance = Email.from_json(json)
# print the JSON string representation of the object
print(Email.to_json())

# convert the object into a dict
email_dict = email_instance.to_dict()
# create an instance of Email from a dict
email_from_dict = Email.from_dict(email_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


