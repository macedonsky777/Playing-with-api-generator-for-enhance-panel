# Subscription

An organization's subscription to a plan. This allows the subscriber to use the subscribed to resources up until the quota defined in the plan is exhausted. Includes details about the subscription as well as the current usage of the resources.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**plan_id** | **int** |  | 
**plan_name** | **str** |  | 
**subscriber_id** | **str** |  | 
**vendor_id** | **str** |  | 
**status** | [**Status**](Status.md) |  | 
**suspended_by** | **str** |  | [optional] 
**resources** | [**List[UsedResource]**](UsedResource.md) | A list of used resources. | 
**allowances** | [**List[Allowance]**](Allowance.md) |  | 
**selections** | [**List[Selection]**](Selection.md) |  | 
**dedicated_servers** | [**SubscriptionDedicatedServersInfo**](SubscriptionDedicatedServersInfo.md) |  | [optional] 
**plan_type** | [**PlanType**](PlanType.md) |  | 
**allowed_php_versions** | [**List[PhpVersion]**](PhpVersion.md) |  | 
**default_php_version** | [**PhpVersion**](PhpVersion.md) |  | 
**redis_allowed** | **bool** |  | 
**server_groups** | [**List[ServerGroup]**](ServerGroup.md) | If this field is present, the customer is allowed to chose from the server groups listed here when creating a website. | [optional] 
**preinstall_wordpress_theme** | **str** | :&gt; When WordPress is installed on a website under this plan, the chosen theme will be preinstalled. | [optional] 
**friendly_name** | **str** |  | 

## Example

```python
from openapi_client.models.subscription import Subscription

# TODO update the JSON string below
json = "{}"
# create an instance of Subscription from a JSON string
subscription_instance = Subscription.from_json(json)
# print the JSON string representation of the object
print(Subscription.to_json())

# convert the object into a dict
subscription_dict = subscription_instance.to_dict()
# create an instance of Subscription from a dict
subscription_from_dict = Subscription.from_dict(subscription_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


