# UpdateSubscription


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | [**Status**](Status.md) |  | [optional] 
**is_suspended** | **bool** |  | [optional] 
**plan_id** | **int** |  | [optional] 
**dedicated_servers** | [**SubscriptionDedicatedServers**](SubscriptionDedicatedServers.md) |  | [optional] 
**friendly_name** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.update_subscription import UpdateSubscription

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateSubscription from a JSON string
update_subscription_instance = UpdateSubscription.from_json(json)
# print the JSON string representation of the object
print(UpdateSubscription.to_json())

# convert the object into a dict
update_subscription_dict = update_subscription_instance.to_dict()
# create an instance of UpdateSubscription from a dict
update_subscription_from_dict = UpdateSubscription.from_dict(update_subscription_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


