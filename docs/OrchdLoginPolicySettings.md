# OrchdLoginPolicySettings

Settings for orchd login policy

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** |  | [optional] 
**email_quota** | **int** |  | [optional] 
**email_auto_block_enabled** | **bool** |  | [optional] 
**email_auto_block_threshold** | **int** |  | [optional] 
**email_auto_block_duration** | **int** |  | [optional] 
**ip_quota** | **int** |  | [optional] 
**ip_auto_block_enabled** | **bool** |  | [optional] 
**ip_auto_block_threshold** | **int** |  | [optional] 
**ip_auto_block_duration** | **int** |  | [optional] 

## Example

```python
from openapi_client.models.orchd_login_policy_settings import OrchdLoginPolicySettings

# TODO update the JSON string below
json = "{}"
# create an instance of OrchdLoginPolicySettings from a JSON string
orchd_login_policy_settings_instance = OrchdLoginPolicySettings.from_json(json)
# print the JSON string representation of the object
print(OrchdLoginPolicySettings.to_json())

# convert the object into a dict
orchd_login_policy_settings_dict = orchd_login_policy_settings_instance.to_dict()
# create an instance of OrchdLoginPolicySettings from a dict
orchd_login_policy_settings_from_dict = OrchdLoginPolicySettings.from_dict(orchd_login_policy_settings_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


