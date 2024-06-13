# PlansListing


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[Plan]**](Plan.md) |  | 
**total** | **int** |  | 

## Example

```python
from openapi_client.models.plans_listing import PlansListing

# TODO update the JSON string below
json = "{}"
# create an instance of PlansListing from a JSON string
plans_listing_instance = PlansListing.from_json(json)
# print the JSON string representation of the object
print(PlansListing.to_json())

# convert the object into a dict
plans_listing_dict = plans_listing_instance.to_dict()
# create an instance of PlansListing from a dict
plans_listing_from_dict = PlansListing.from_dict(plans_listing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


