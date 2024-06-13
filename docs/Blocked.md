# Blocked


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**blocked_until** | **int** |  | [optional] 
**current_failures** | **int** |  | [optional] 
**all_failures** | **int** |  | [optional] 

## Example

```python
from openapi_client.models.blocked import Blocked

# TODO update the JSON string below
json = "{}"
# create an instance of Blocked from a JSON string
blocked_instance = Blocked.from_json(json)
# print the JSON string representation of the object
print(Blocked.to_json())

# convert the object into a dict
blocked_dict = blocked_instance.to_dict()
# create an instance of Blocked from a dict
blocked_from_dict = Blocked.from_dict(blocked_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


