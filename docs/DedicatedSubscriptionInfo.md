# DedicatedSubscriptionInfo


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subscription_id** | **float** |  | 
**customer_org_id** | **str** |  | 
**customer_org_name** | **str** |  | 

## Example

```python
from openapi_client.models.dedicated_subscription_info import DedicatedSubscriptionInfo

# TODO update the JSON string below
json = "{}"
# create an instance of DedicatedSubscriptionInfo from a JSON string
dedicated_subscription_info_instance = DedicatedSubscriptionInfo.from_json(json)
# print the JSON string representation of the object
print(DedicatedSubscriptionInfo.to_json())

# convert the object into a dict
dedicated_subscription_info_dict = dedicated_subscription_info_instance.to_dict()
# create an instance of DedicatedSubscriptionInfo from a dict
dedicated_subscription_info_from_dict = DedicatedSubscriptionInfo.from_dict(dedicated_subscription_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


