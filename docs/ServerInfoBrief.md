# ServerInfoBrief


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**group_id** | **str** |  | 
**is_control_panel** | **bool** |  | 
**is_configured** | **bool** |  | 
**friendly_name** | **str** |  | 
**hostname** | **str** |  | 
**ips** | [**List[ServerIp]**](ServerIp.md) |  | 
**roles** | [**RoleInstalledStatusSummary**](RoleInstalledStatusSummary.md) |  | 
**created_at** | **str** |  | 
**dedicated_subscription** | **float** |  | [optional] 
**is_decommissioned** | **bool** |  | 
**ipv6_addr** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.server_info_brief import ServerInfoBrief

# TODO update the JSON string below
json = "{}"
# create an instance of ServerInfoBrief from a JSON string
server_info_brief_instance = ServerInfoBrief.from_json(json)
# print the JSON string representation of the object
print(ServerInfoBrief.to_json())

# convert the object into a dict
server_info_brief_dict = server_info_brief_instance.to_dict()
# create an instance of ServerInfoBrief from a dict
server_info_brief_from_dict = ServerInfoBrief.from_dict(server_info_brief_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


