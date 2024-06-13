# SetCgroupLimits


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**nproc** | **float** |  | [optional] 
**memory_limit** | **float** |  | [optional] 
**iops** | **float** |  | [optional] 
**io_bandwidth** | **float** |  | [optional] 
**virtual_cpus** | **float** |  | [optional] 

## Example

```python
from openapi_client.models.set_cgroup_limits import SetCgroupLimits

# TODO update the JSON string below
json = "{}"
# create an instance of SetCgroupLimits from a JSON string
set_cgroup_limits_instance = SetCgroupLimits.from_json(json)
# print the JSON string representation of the object
print(SetCgroupLimits.to_json())

# convert the object into a dict
set_cgroup_limits_dict = set_cgroup_limits_instance.to_dict()
# create an instance of SetCgroupLimits from a dict
set_cgroup_limits_from_dict = SetCgroupLimits.from_dict(set_cgroup_limits_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


