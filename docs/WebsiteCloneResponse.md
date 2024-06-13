# WebsiteCloneResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**source_website_id** | **str** |  | 
**dest_website_id** | **str** |  | [optional] 
**exclude_paths** | **List[str]** |  | 
**include_databases** | **List[str]** |  | 
**include_database_users** | **List[str]** |  | 
**delete_files_from_destination** | **bool** |  | 
**status** | [**WebsiteCloneEnumStatus**](WebsiteCloneEnumStatus.md) |  | 
**sync_php_version** | **bool** |  | 

## Example

```python
from openapi_client.models.website_clone_response import WebsiteCloneResponse

# TODO update the JSON string below
json = "{}"
# create an instance of WebsiteCloneResponse from a JSON string
website_clone_response_instance = WebsiteCloneResponse.from_json(json)
# print the JSON string representation of the object
print(WebsiteCloneResponse.to_json())

# convert the object into a dict
website_clone_response_dict = website_clone_response_instance.to_dict()
# create an instance of WebsiteCloneResponse from a dict
website_clone_response_from_dict = WebsiteCloneResponse.from_dict(website_clone_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


