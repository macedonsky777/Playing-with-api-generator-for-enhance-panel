# OrgUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**status** | [**Status**](Status.md) |  | [optional] 
**is_suspended** | **bool** |  | [optional] 
**locale** | [**CPLocale**](CPLocale.md) |  | [optional] 
**slack_notification_webhook_url** | [**OrgUpdateSlackNotificationWebhookUrl**](OrgUpdateSlackNotificationWebhookUrl.md) |  | [optional] 

## Example

```python
from openapi_client.models.org_update import OrgUpdate

# TODO update the JSON string below
json = "{}"
# create an instance of OrgUpdate from a JSON string
org_update_instance = OrgUpdate.from_json(json)
# print the JSON string representation of the object
print(OrgUpdate.to_json())

# convert the object into a dict
org_update_dict = org_update_instance.to_dict()
# create an instance of OrgUpdate from a dict
org_update_from_dict = OrgUpdate.from_dict(org_update_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


