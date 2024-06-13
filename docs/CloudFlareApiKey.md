# CloudFlareApiKey


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**token** | **str** |  | 
**updated_at** | **date** |  | 
**friendly_name** | **str** |  | 
**last_sync** | **date** |  | [optional] 
**last_message** | **str** |  | [optional] 
**domains** | **List[str]** |  | [optional] 

## Example

```python
from openapi_client.models.cloud_flare_api_key import CloudFlareApiKey

# TODO update the JSON string below
json = "{}"
# create an instance of CloudFlareApiKey from a JSON string
cloud_flare_api_key_instance = CloudFlareApiKey.from_json(json)
# print the JSON string representation of the object
print(CloudFlareApiKey.to_json())

# convert the object into a dict
cloud_flare_api_key_dict = cloud_flare_api_key_instance.to_dict()
# create an instance of CloudFlareApiKey from a dict
cloud_flare_api_key_from_dict = CloudFlareApiKey.from_dict(cloud_flare_api_key_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


