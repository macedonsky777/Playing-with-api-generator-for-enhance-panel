# FsQuotaLimit

File system quota settings in bytes.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_available** | **float** |  | 

## Example

```python
from openapi_client.models.fs_quota_limit import FsQuotaLimit

# TODO update the JSON string below
json = "{}"
# create an instance of FsQuotaLimit from a JSON string
fs_quota_limit_instance = FsQuotaLimit.from_json(json)
# print the JSON string representation of the object
print(FsQuotaLimit.to_json())

# convert the object into a dict
fs_quota_limit_dict = fs_quota_limit_instance.to_dict()
# create an instance of FsQuotaLimit from a dict
fs_quota_limit_from_dict = FsQuotaLimit.from_dict(fs_quota_limit_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


