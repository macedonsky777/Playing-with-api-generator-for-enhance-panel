# ServerHostnameWebsite


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**website_id** | **str** |  | 
**domains** | [**List[DomainWithUuid]**](DomainWithUuid.md) |  | 

## Example

```python
from openapi_client.models.server_hostname_website import ServerHostnameWebsite

# TODO update the JSON string below
json = "{}"
# create an instance of ServerHostnameWebsite from a JSON string
server_hostname_website_instance = ServerHostnameWebsite.from_json(json)
# print the JSON string representation of the object
print(ServerHostnameWebsite.to_json())

# convert the object into a dict
server_hostname_website_dict = server_hostname_website_instance.to_dict()
# create an instance of ServerHostnameWebsite from a dict
server_hostname_website_from_dict = ServerHostnameWebsite.from_dict(server_hostname_website_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


