# Plan

A plan (or sometimes referred to as a package) defines a set of resources a reseller can offer for customer organizations to subscribe to.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**name** | **str** |  | 
**org_id** | **str** |  | 
**resources** | [**List[Resource]**](Resource.md) |  | 
**allowances** | [**List[Allowance]**](Allowance.md) |  | 
**selections** | [**List[Selection]**](Selection.md) |  | 
**subscriptions_count** | **int** | The number of subscriptions to this plan. | 
**server_group_id** | **str** | Use serverGroupIds instead | [optional] 
**server_group_ids** | **List[str]** |  | [optional] 
**allow_server_group_selection** | **bool** | Whether the customer can select the server group for their websites.  | [optional] 
**created_at** | **str** |  | 
**plan_type** | [**PlanType**](PlanType.md) |  | 
**cgroup_limits** | [**CgroupLimits**](CgroupLimits.md) |  | [optional] 
**fs_quota_limit** | [**FsQuotaLimit**](FsQuotaLimit.md) |  | [optional] 
**allowed_php_versions** | [**List[PhpVersion]**](PhpVersion.md) |  | 
**default_php_version** | [**PhpVersion**](PhpVersion.md) |  | 
**redis_allowed** | **bool** |  | 
**preinstall_wordpress_theme** | **str** | :&gt; When WordPress is installed on a website under this plan, the chosen theme will be preinstalled. | [optional] 

## Example

```python
from openapi_client.models.plan import Plan

# TODO update the JSON string below
json = "{}"
# create an instance of Plan from a JSON string
plan_instance = Plan.from_json(json)
# print the JSON string representation of the object
print(Plan.to_json())

# convert the object into a dict
plan_dict = plan_instance.to_dict()
# create an instance of Plan from a dict
plan_from_dict = Plan.from_dict(plan_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


