# SubscriptionDedicatedServers


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**app_server_id** | **str** |  | [optional] 
**backup_server_id** | **str** |  | [optional] 
**db_server_id** | **str** |  | [optional] 
**email_server_id** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.subscription_dedicated_servers import SubscriptionDedicatedServers

# TODO update the JSON string below
json = "{}"
# create an instance of SubscriptionDedicatedServers from a JSON string
subscription_dedicated_servers_instance = SubscriptionDedicatedServers.from_json(json)
# print the JSON string representation of the object
print(SubscriptionDedicatedServers.to_json())

# convert the object into a dict
subscription_dedicated_servers_dict = subscription_dedicated_servers_instance.to_dict()
# create an instance of SubscriptionDedicatedServers from a dict
subscription_dedicated_servers_from_dict = SubscriptionDedicatedServers.from_dict(subscription_dedicated_servers_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


