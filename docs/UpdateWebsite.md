# UpdateWebsite


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**php_version** | [**PhpVersion**](PhpVersion.md) |  | [optional] 
**status** | [**WebsiteStatus**](WebsiteStatus.md) |  | [optional] 
**is_suspended** | **bool** |  | [optional] 
**tags** | **List[int]** |  | [optional] 
**subscription_id** | [**UpdateWebsiteSubscriptionId**](UpdateWebsiteSubscriptionId.md) |  | [optional] 
**org_id** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.update_website import UpdateWebsite

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateWebsite from a JSON string
update_website_instance = UpdateWebsite.from_json(json)
# print the JSON string representation of the object
print(UpdateWebsite.to_json())

# convert the object into a dict
update_website_dict = update_website_instance.to_dict()
# create an instance of UpdateWebsite from a dict
update_website_from_dict = UpdateWebsite.from_dict(update_website_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


