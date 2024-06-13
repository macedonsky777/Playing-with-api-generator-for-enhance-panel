# ActivityContextActor


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | 
**content** | [**ActivityLoginEntityContent**](ActivityLoginEntityContent.md) |  | 

## Example

```python
from openapi_client.models.activity_context_actor import ActivityContextActor

# TODO update the JSON string below
json = "{}"
# create an instance of ActivityContextActor from a JSON string
activity_context_actor_instance = ActivityContextActor.from_json(json)
# print the JSON string representation of the object
print(ActivityContextActor.to_json())

# convert the object into a dict
activity_context_actor_dict = activity_context_actor_instance.to_dict()
# create an instance of ActivityContextActor from a dict
activity_context_actor_from_dict = ActivityContextActor.from_dict(activity_context_actor_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


