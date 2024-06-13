# UpdatePlan


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**plan_type** | [**PlanType**](PlanType.md) |  | [optional] 
**cgroup_limits** | [**CgroupLimits**](CgroupLimits.md) |  | [optional] 
**fs_quota_limit** | [**FsQuotaLimit**](FsQuotaLimit.md) |  | [optional] 
**allowed_php_versions** | [**List[PhpVersion]**](PhpVersion.md) |  | [optional] 
**default_php_version** | [**PhpVersion**](PhpVersion.md) |  | [optional] 
**redis_allowed** | **bool** |  | [optional] 
**server_group_ids** | **List[str]** | If provided as an empty array, removes all server groups from the plan.  | [optional] 
**allow_server_group_selection** | **bool** | Whether the customer can select the server group for their websites.  | [optional] 
**default_server_group_id** | [**UpdatePlanDefaultServerGroupId**](UpdatePlanDefaultServerGroupId.md) |  | [optional] 
**preinstall_wordpress_theme** | **str** | :&gt; When WordPress is installed on a website under this plan, the chosen theme will be preinstalled. | [optional] 

## Example

```python
from openapi_client.models.update_plan import UpdatePlan

# TODO update the JSON string below
json = "{}"
# create an instance of UpdatePlan from a JSON string
update_plan_instance = UpdatePlan.from_json(json)
# print the JSON string representation of the object
print(UpdatePlan.to_json())

# convert the object into a dict
update_plan_dict = update_plan_instance.to_dict()
# create an instance of UpdatePlan from a dict
update_plan_from_dict = UpdatePlan.from_dict(update_plan_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


