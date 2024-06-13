# SubscriptionsListing


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[Subscription]**](Subscription.md) |  | 
**total** | **int** |  | 

## Example

```python
from openapi_client.models.subscriptions_listing import SubscriptionsListing

# TODO update the JSON string below
json = "{}"
# create an instance of SubscriptionsListing from a JSON string
subscriptions_listing_instance = SubscriptionsListing.from_json(json)
# print the JSON string representation of the object
print(SubscriptionsListing.to_json())

# convert the object into a dict
subscriptions_listing_dict = subscriptions_listing_instance.to_dict()
# create an instance of SubscriptionsListing from a dict
subscriptions_listing_from_dict = SubscriptionsListing.from_dict(subscriptions_listing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


