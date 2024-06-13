# UpdatePlanDefaultServerGroupId

If set, servers from this server group are prioritized by placement algorithm. If no server from the default server group is available, servers from other server groups are tried. If both serverGroupIds and defaultServerGroupId is provided, defaultServerGroupId will be added to serverGroupIds if not there. If only defaultServerGroupId is provided, already existing plan's serverGroupIds will be expanded with defaultServerGroupId if not there yet. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**unset** | **bool** |  | 

## Example

```python
from openapi_client.models.update_plan_default_server_group_id import UpdatePlanDefaultServerGroupId

# TODO update the JSON string below
json = "{}"
# create an instance of UpdatePlanDefaultServerGroupId from a JSON string
update_plan_default_server_group_id_instance = UpdatePlanDefaultServerGroupId.from_json(json)
# print the JSON string representation of the object
print(UpdatePlanDefaultServerGroupId.to_json())

# convert the object into a dict
update_plan_default_server_group_id_dict = update_plan_default_server_group_id_instance.to_dict()
# create an instance of UpdatePlanDefaultServerGroupId from a dict
update_plan_default_server_group_id_from_dict = UpdatePlanDefaultServerGroupId.from_dict(update_plan_default_server_group_id_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


