# CgroupLimits


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**nproc** | **float** |  | 
**memory_limit** | **float** |  | 
**iops** | **float** |  | 
**io_bandwidth** | **float** |  | 
**virtual_cpus** | **float** |  | 

## Example

```python
from openapi_client.models.cgroup_limits import CgroupLimits

# TODO update the JSON string below
json = "{}"
# create an instance of CgroupLimits from a JSON string
cgroup_limits_instance = CgroupLimits.from_json(json)
# print the JSON string representation of the object
print(CgroupLimits.to_json())

# convert the object into a dict
cgroup_limits_dict = cgroup_limits_instance.to_dict()
# create an instance of CgroupLimits from a dict
cgroup_limits_from_dict = CgroupLimits.from_dict(cgroup_limits_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


