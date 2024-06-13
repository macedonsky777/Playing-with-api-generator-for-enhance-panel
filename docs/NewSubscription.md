# NewSubscription


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**plan_id** | **int** |  | 
**dedicated_servers** | [**SubscriptionDedicatedServers**](SubscriptionDedicatedServers.md) |  | [optional] 
**friendly_name** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.new_subscription import NewSubscription

# TODO update the JSON string below
json = "{}"
# create an instance of NewSubscription from a JSON string
new_subscription_instance = NewSubscription.from_json(json)
# print the JSON string representation of the object
print(NewSubscription.to_json())

# convert the object into a dict
new_subscription_dict = new_subscription_instance.to_dict()
# create an instance of NewSubscription from a dict
new_subscription_from_dict = NewSubscription.from_dict(new_subscription_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


