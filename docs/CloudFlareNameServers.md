# CloudFlareNameServers


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name_servers** | **List[str]** |  | 
**status** | **str** |  | 

## Example

```python
from openapi_client.models.cloud_flare_name_servers import CloudFlareNameServers

# TODO update the JSON string below
json = "{}"
# create an instance of CloudFlareNameServers from a JSON string
cloud_flare_name_servers_instance = CloudFlareNameServers.from_json(json)
# print the JSON string representation of the object
print(CloudFlareNameServers.to_json())

# convert the object into a dict
cloud_flare_name_servers_dict = cloud_flare_name_servers_instance.to_dict()
# create an instance of CloudFlareNameServers from a dict
cloud_flare_name_servers_from_dict = CloudFlareNameServers.from_dict(cloud_flare_name_servers_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


