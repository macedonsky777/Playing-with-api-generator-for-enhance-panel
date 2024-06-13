# UpdateCrontabValueCmd


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cron_cmd** | [**UpdateCrontabValueCmdCronCmd**](UpdateCrontabValueCmdCronCmd.md) |  | 

## Example

```python
from openapi_client.models.update_crontab_value_cmd import UpdateCrontabValueCmd

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateCrontabValueCmd from a JSON string
update_crontab_value_cmd_instance = UpdateCrontabValueCmd.from_json(json)
# print the JSON string representation of the object
print(UpdateCrontabValueCmd.to_json())

# convert the object into a dict
update_crontab_value_cmd_dict = update_crontab_value_cmd_instance.to_dict()
# create an instance of UpdateCrontabValueCmd from a dict
update_crontab_value_cmd_from_dict = UpdateCrontabValueCmd.from_dict(update_crontab_value_cmd_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


