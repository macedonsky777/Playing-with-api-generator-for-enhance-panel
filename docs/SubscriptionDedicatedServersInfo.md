# SubscriptionDedicatedServersInfo


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**app_server** | [**SubscriptionDedicatedServer**](SubscriptionDedicatedServer.md) |  | [optional] 
**backup_server** | [**SubscriptionDedicatedServer**](SubscriptionDedicatedServer.md) |  | [optional] 
**db_server** | [**SubscriptionDedicatedServer**](SubscriptionDedicatedServer.md) |  | [optional] 
**email_server** | [**SubscriptionDedicatedServer**](SubscriptionDedicatedServer.md) |  | [optional] 

## Example

```python
from openapi_client.models.subscription_dedicated_servers_info import SubscriptionDedicatedServersInfo

# TODO update the JSON string below
json = "{}"
# create an instance of SubscriptionDedicatedServersInfo from a JSON string
subscription_dedicated_servers_info_instance = SubscriptionDedicatedServersInfo.from_json(json)
# print the JSON string representation of the object
print(SubscriptionDedicatedServersInfo.to_json())

# convert the object into a dict
subscription_dedicated_servers_info_dict = subscription_dedicated_servers_info_instance.to_dict()
# create an instance of SubscriptionDedicatedServersInfo from a dict
subscription_dedicated_servers_info_from_dict = SubscriptionDedicatedServersInfo.from_dict(subscription_dedicated_servers_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


