# FsQuotaInfo

File system quota info in bytes.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_available** | **float** |  | 
**used** | **float** |  | [optional] 

## Example

```python
from openapi_client.models.fs_quota_info import FsQuotaInfo

# TODO update the JSON string below
json = "{}"
# create an instance of FsQuotaInfo from a JSON string
fs_quota_info_instance = FsQuotaInfo.from_json(json)
# print the JSON string representation of the object
print(FsQuotaInfo.to_json())

# convert the object into a dict
fs_quota_info_dict = fs_quota_info_instance.to_dict()
# create an instance of FsQuotaInfo from a dict
fs_quota_info_from_dict = FsQuotaInfo.from_dict(fs_quota_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


