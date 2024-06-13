# WebsiteCloneRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**run_wp_search_replace** | **bool** |  | [optional] 
**source_website_id** | **str** |  | 
**dest_website_id** | **str** |  | [optional] 
**exclude_paths** | **List[str]** |  | 
**include_databases** | **List[str]** |  | [optional] 
**include_database_users** | **List[str]** |  | [optional] 
**delete_files_from_destination** | **bool** |  | 
**sync_php_version** | **bool** |  | 
**new_website** | [**WebsiteCloneNewWebsite**](WebsiteCloneNewWebsite.md) |  | [optional] 

## Example

```python
from openapi_client.models.website_clone_request import WebsiteCloneRequest

# TODO update the JSON string below
json = "{}"
# create an instance of WebsiteCloneRequest from a JSON string
website_clone_request_instance = WebsiteCloneRequest.from_json(json)
# print the JSON string representation of the object
print(WebsiteCloneRequest.to_json())

# convert the object into a dict
website_clone_request_dict = website_clone_request_instance.to_dict()
# create an instance of WebsiteCloneRequest from a dict
website_clone_request_from_dict = WebsiteCloneRequest.from_dict(website_clone_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


