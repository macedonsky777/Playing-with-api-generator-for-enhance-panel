# WebsiteCloneLogEntry


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_at** | **datetime** |  | 
**message** | **str** |  | 
**percentage_complete** | **float** |  | 

## Example

```python
from openapi_client.models.website_clone_log_entry import WebsiteCloneLogEntry

# TODO update the JSON string below
json = "{}"
# create an instance of WebsiteCloneLogEntry from a JSON string
website_clone_log_entry_instance = WebsiteCloneLogEntry.from_json(json)
# print the JSON string representation of the object
print(WebsiteCloneLogEntry.to_json())

# convert the object into a dict
website_clone_log_entry_dict = website_clone_log_entry_instance.to_dict()
# create an instance of WebsiteCloneLogEntry from a dict
website_clone_log_entry_from_dict = WebsiteCloneLogEntry.from_dict(website_clone_log_entry_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


