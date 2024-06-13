# EmailDetailed


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**mailbox_name** | **str** |  | [optional] 
**address** | **str** |  | 
**aliases** | **List[str]** |  | 
**forwarders** | **List[str]** |  | [optional] 
**mailbox_id** | **str** |  | [optional] 
**status** | [**WebsiteStatus**](WebsiteStatus.md) |  | 
**quota** | [**Quota**](Quota.md) |  | [optional] 
**spam_threshold** | **int** |  | [optional] 
**spam_delivery** | **str** |  | 
**blacklist** | **List[str]** |  | 
**whitelist** | **List[str]** |  | 
**autoresponders_count** | **int** |  | 
**created_at** | **str** |  | 

## Example

```python
from openapi_client.models.email_detailed import EmailDetailed

# TODO update the JSON string below
json = "{}"
# create an instance of EmailDetailed from a JSON string
email_detailed_instance = EmailDetailed.from_json(json)
# print the JSON string representation of the object
print(EmailDetailed.to_json())

# convert the object into a dict
email_detailed_dict = email_detailed_instance.to_dict()
# create an instance of EmailDetailed from a dict
email_detailed_from_dict = EmailDetailed.from_dict(email_detailed_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


