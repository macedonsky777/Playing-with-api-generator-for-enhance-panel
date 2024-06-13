# ServerInfo


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
**disks** | [**List[Disk]**](Disk.md) |  | [optional] 
**os_usage** | **int** |  | [optional] 
**status** | [**NetworkStatus**](NetworkStatus.md) |  | [optional] 
**roles** | [**RolesSummary**](RolesSummary.md) |  | 
**created_at** | **str** |  | 
**controld_version** | **str** |  | [optional] 
**dedicated_subscription** | [**DedicatedSubscriptionInfo**](DedicatedSubscriptionInfo.md) |  | [optional] 
**is_decommissioned** | **bool** |  | 
**ipv6_addr** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.server_info import ServerInfo

# TODO update the JSON string below
json = "{}"
# create an instance of ServerInfo from a JSON string
server_info_instance = ServerInfo.from_json(json)
# print the JSON string representation of the object
print(ServerInfo.to_json())

# convert the object into a dict
server_info_dict = server_info_instance.to_dict()
# create an instance of ServerInfo from a dict
server_info_from_dict = ServerInfo.from_dict(server_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


