# UpdateCrontabValue


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**variable** | [**UpdateCrontabValueVariableVariable**](UpdateCrontabValueVariableVariable.md) |  | 
**cron_cmd** | [**UpdateCrontabValueCmdCronCmd**](UpdateCrontabValueCmdCronCmd.md) |  | 

## Example

```python
from openapi_client.models.update_crontab_value import UpdateCrontabValue

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateCrontabValue from a JSON string
update_crontab_value_instance = UpdateCrontabValue.from_json(json)
# print the JSON string representation of the object
print(UpdateCrontabValue.to_json())

# convert the object into a dict
update_crontab_value_dict = update_crontab_value_instance.to_dict()
# create an instance of UpdateCrontabValue from a dict
update_crontab_value_from_dict = UpdateCrontabValue.from_dict(update_crontab_value_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


