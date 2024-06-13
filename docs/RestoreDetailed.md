# RestoreDetailed


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**backup_id** | **int** |  | 
**started_at** | **datetime** |  | 
**finished_at** | **datetime** |  | [optional] 
**home_dir_status** | [**OperationStatus**](OperationStatus.md) |  | [optional] 
**mysql_dbs_status** | [**OperationStatus**](OperationStatus.md) |  | [optional] 
**emails_status** | [**OperationStatus**](OperationStatus.md) |  | [optional] 

## Example

```python
from openapi_client.models.restore_detailed import RestoreDetailed

# TODO update the JSON string below
json = "{}"
# create an instance of RestoreDetailed from a JSON string
restore_detailed_instance = RestoreDetailed.from_json(json)
# print the JSON string representation of the object
print(RestoreDetailed.to_json())

# convert the object into a dict
restore_detailed_dict = restore_detailed_instance.to_dict()
# create an instance of RestoreDetailed from a dict
restore_detailed_from_dict = RestoreDetailed.from_dict(restore_detailed_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


