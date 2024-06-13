# ActivityContext


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**org** | [**ActivityOrgEntity**](ActivityOrgEntity.md) |  | [optional] 
**website** | [**ActivityWebsiteEntity**](ActivityWebsiteEntity.md) |  | [optional] 
**domain** | [**ActivityDomainEntity**](ActivityDomainEntity.md) |  | [optional] 
**actor** | [**ActivityContextActor**](ActivityContextActor.md) |  | [optional] 
**server** | [**ActivityServerEntity**](ActivityServerEntity.md) |  | [optional] 
**error** | [**ActivityErrorEntity**](ActivityErrorEntity.md) |  | [optional] 

## Example

```python
from openapi_client.models.activity_context import ActivityContext

# TODO update the JSON string below
json = "{}"
# create an instance of ActivityContext from a JSON string
activity_context_instance = ActivityContext.from_json(json)
# print the JSON string representation of the object
print(ActivityContext.to_json())

# convert the object into a dict
activity_context_dict = activity_context_instance.to_dict()
# create an instance of ActivityContext from a dict
activity_context_from_dict = ActivityContext.from_dict(activity_context_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


