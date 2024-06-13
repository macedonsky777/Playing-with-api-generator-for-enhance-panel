# NewWebsite


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **str** | The domain of the new website. | 
**subscription_id** | **int** |  | [optional] 
**app_server_id** | **str** |  | [optional] 
**backup_server_id** | **str** |  | [optional] 
**db_server_id** | **str** |  | [optional] 
**email_server_id** | **str** |  | [optional] 
**server_group_id** | **str** |  | [optional] 
**php_version** | [**PhpVersion**](PhpVersion.md) |  | [optional] 

## Example

```python
from openapi_client.models.new_website import NewWebsite

# TODO update the JSON string below
json = "{}"
# create an instance of NewWebsite from a JSON string
new_website_instance = NewWebsite.from_json(json)
# print the JSON string representation of the object
print(NewWebsite.to_json())

# convert the object into a dict
new_website_dict = new_website_instance.to_dict()
# create an instance of NewWebsite from a dict
new_website_from_dict = NewWebsite.from_dict(new_website_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


