# ResourceCountByInterval


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**interval** | **str** |  | 
**resource_count** | **float** |  | 

## Example

```python
from openapi_client.models.resource_count_by_interval import ResourceCountByInterval

# TODO update the JSON string below
json = "{}"
# create an instance of ResourceCountByInterval from a JSON string
resource_count_by_interval_instance = ResourceCountByInterval.from_json(json)
# print the JSON string representation of the object
print(ResourceCountByInterval.to_json())

# convert the object into a dict
resource_count_by_interval_dict = resource_count_by_interval_instance.to_dict()
# create an instance of ResourceCountByInterval from a dict
resource_count_by_interval_from_dict = ResourceCountByInterval.from_dict(resource_count_by_interval_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


