# Org


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**parent_id** | **str** |  | [optional] 
**name** | **str** |  | 
**status** | [**Status**](Status.md) |  | 
**suspended_by** | **str** |  | [optional] 
**owner** | **str** |  | [optional] 
**owner_email** | **str** |  | [optional] 
**owner_id** | **str** |  | [optional] 
**owner_login_id** | **str** |  | [optional] 
**subscriptions_count** | **int** |  | 
**websites_count** | **int** |  | 
**created_at** | **str** |  | 
**owner_avatar_path** | **str** |  | [optional] 
**locale** | [**CPLocale**](CPLocale.md) |  | 
**slack_notification_webhook_url** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.org import Org

# TODO update the JSON string below
json = "{}"
# create an instance of Org from a JSON string
org_instance = Org.from_json(json)
# print the JSON string representation of the object
print(Org.to_json())

# convert the object into a dict
org_dict = org_instance.to_dict()
# create an instance of Org from a dict
org_from_dict = Org.from_dict(org_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


