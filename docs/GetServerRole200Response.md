# GetServerRole200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**state** | [**ServerRoleState**](ServerRoleState.md) |  | 
**usage** | **int** |  | 
**mailbox_count** | **int** |  | 
**failed_delivery_count** | **int** |  | 
**mtacd** | [**ServiceInfo**](ServiceInfo.md) |  | 
**imapcd** | [**ServiceInfo**](ServiceInfo.md) |  | 
**spamcd** | [**ServiceInfo**](ServiceInfo.md) |  | 
**websites_count** | **int** | The number of websites whose DNS zones are assigned to be on this dns role. | 
**snapshots_count** | **int** |  | 
**last24h_snapshots_count** | **int** |  | 
**bkupd** | [**ServiceInfo**](ServiceInfo.md) |  | 
**mysql_stats** | **object** |  | 
**mysqlcd** | [**ServiceInfo**](ServiceInfo.md) |  | 
**filerd** | [**ServiceInfo**](ServiceInfo.md) |  | 
**ftpcd** | [**ServiceInfo**](ServiceInfo.md) |  | 
**zones_count** | **int** |  | 
**dnscd** | [**ServiceInfo**](ServiceInfo.md) |  | 

## Example

```python
from openapi_client.models.get_server_role200_response import GetServerRole200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetServerRole200Response from a JSON string
get_server_role200_response_instance = GetServerRole200Response.from_json(json)
# print the JSON string representation of the object
print(GetServerRole200Response.to_json())

# convert the object into a dict
get_server_role200_response_dict = get_server_role200_response_instance.to_dict()
# create an instance of GetServerRole200Response from a dict
get_server_role200_response_from_dict = GetServerRole200Response.from_dict(get_server_role200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


