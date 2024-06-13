# ChangeSubscriptionParams


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subscription_id** | [**ChangeSubscriptionParamsSubscriptionId**](ChangeSubscriptionParamsSubscriptionId.md) |  | 

## Example

```python
from openapi_client.models.change_subscription_params import ChangeSubscriptionParams

# TODO update the JSON string below
json = "{}"
# create an instance of ChangeSubscriptionParams from a JSON string
change_subscription_params_instance = ChangeSubscriptionParams.from_json(json)
# print the JSON string representation of the object
print(ChangeSubscriptionParams.to_json())

# convert the object into a dict
change_subscription_params_dict = change_subscription_params_instance.to_dict()
# create an instance of ChangeSubscriptionParams from a dict
change_subscription_params_from_dict = ChangeSubscriptionParams.from_dict(change_subscription_params_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


