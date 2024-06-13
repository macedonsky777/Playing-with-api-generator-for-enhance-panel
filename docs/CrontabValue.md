# CrontabValue


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**variable** | [**CrontabValueVariableVariable**](CrontabValueVariableVariable.md) |  | 
**cron_cmd** | [**CrontabValueCmdCronCmd**](CrontabValueCmdCronCmd.md) |  | 

## Example

```python
from openapi_client.models.crontab_value import CrontabValue

# TODO update the JSON string below
json = "{}"
# create an instance of CrontabValue from a JSON string
crontab_value_instance = CrontabValue.from_json(json)
# print the JSON string representation of the object
print(CrontabValue.to_json())

# convert the object into a dict
crontab_value_dict = crontab_value_instance.to_dict()
# create an instance of CrontabValue from a dict
crontab_value_from_dict = CrontabValue.from_dict(crontab_value_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


