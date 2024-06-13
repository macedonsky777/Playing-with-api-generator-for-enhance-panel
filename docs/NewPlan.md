# NewPlan


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**resources** | [**List[Resource]**](Resource.md) |  | 
**allowances** | [**List[Allowance]**](Allowance.md) |  | 
**selections** | [**List[Selection]**](Selection.md) |  | 
**server_group_id** | **str** |  | [optional] 
**server_group_ids** | **List[str]** |  | [optional] 
**allow_server_group_selection** | **bool** |  | [optional] 
**plan_type** | [**PlanType**](PlanType.md) |  | [optional] 
**cgroup_limits** | [**CgroupLimits**](CgroupLimits.md) |  | [optional] 
**fs_quota_limit** | [**FsQuotaLimit**](FsQuotaLimit.md) |  | [optional] 
**allowed_php_versions** | [**List[PhpVersion]**](PhpVersion.md) |  | [optional] 
**default_php_version** | [**PhpVersion**](PhpVersion.md) |  | [optional] 
**redis_allowed** | **bool** |  | [optional] 
**default_server_group_id** | **str** | If set, servers from this server group are prioritized by placement algorithm. If no server from the default server group is available, servers from other server groups are tried. The defaultServerGroupId will be automatically added to serverGroupIds if they do not contain it or are not provided.  | [optional] 
**preinstall_wordpress_theme** | **str** | :&gt; When WordPress is installed on a website under this plan, the chosen theme will be preinstalled. | [optional] 

## Example

```python
from openapi_client.models.new_plan import NewPlan

# TODO update the JSON string below
json = "{}"
# create an instance of NewPlan from a JSON string
new_plan_instance = NewPlan.from_json(json)
# print the JSON string representation of the object
print(NewPlan.to_json())

# convert the object into a dict
new_plan_dict = new_plan_instance.to_dict()
# create an instance of NewPlan from a dict
new_plan_from_dict = NewPlan.from_dict(new_plan_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


