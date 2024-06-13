# NewWebsiteApp


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**app** | [**WebsiteAppKind**](WebsiteAppKind.md) |  | 
**version** | **str** |  | [optional] 
**path** | **str** |  | [optional] 
**admin_username** | **str** | This username is going to be the username of the initial WP user with which the user can login to the WP admin. This is equivalent to going to &#x60;wp-admin/install.php&#x60; and performing the install from there. | 
**admin_password** | **str** | Complements the admin username. Provide unhashed password. | 
**admin_email** | **str** | Sets the admin email address, required by some applications. | 
**domain_id** | **str** | Install on a specific domain within this website.  Will default to use the primary domain. | [optional] 

## Example

```python
from openapi_client.models.new_website_app import NewWebsiteApp

# TODO update the JSON string below
json = "{}"
# create an instance of NewWebsiteApp from a JSON string
new_website_app_instance = NewWebsiteApp.from_json(json)
# print the JSON string representation of the object
print(NewWebsiteApp.to_json())

# convert the object into a dict
new_website_app_dict = new_website_app_instance.to_dict()
# create an instance of NewWebsiteApp from a dict
new_website_app_from_dict = NewWebsiteApp.from_dict(new_website_app_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


