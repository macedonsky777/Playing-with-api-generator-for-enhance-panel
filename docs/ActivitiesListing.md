# ActivitiesListing


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total** | **int** |  | 
**items** | [**List[Activity]**](Activity.md) |  | 

## Example

```python
from openapi_client.models.activities_listing import ActivitiesListing

# TODO update the JSON string below
json = "{}"
# create an instance of ActivitiesListing from a JSON string
activities_listing_instance = ActivitiesListing.from_json(json)
# print the JSON string representation of the object
print(ActivitiesListing.to_json())

# convert the object into a dict
activities_listing_dict = activities_listing_instance.to_dict()
# create an instance of ActivitiesListing from a dict
activities_listing_from_dict = ActivitiesListing.from_dict(activities_listing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


