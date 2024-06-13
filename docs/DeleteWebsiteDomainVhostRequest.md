# DeleteWebsiteDomainVhostRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**webserver** | [**VhostWebserverKind**](VhostWebserverKind.md) |  | 

## Example

```python
from openapi_client.models.delete_website_domain_vhost_request import DeleteWebsiteDomainVhostRequest

# TODO update the JSON string below
json = "{}"
# create an instance of DeleteWebsiteDomainVhostRequest from a JSON string
delete_website_domain_vhost_request_instance = DeleteWebsiteDomainVhostRequest.from_json(json)
# print the JSON string representation of the object
print(DeleteWebsiteDomainVhostRequest.to_json())

# convert the object into a dict
delete_website_domain_vhost_request_dict = delete_website_domain_vhost_request_instance.to_dict()
# create an instance of DeleteWebsiteDomainVhostRequest from a dict
delete_website_domain_vhost_request_from_dict = DeleteWebsiteDomainVhostRequest.from_dict(delete_website_domain_vhost_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


