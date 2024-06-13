# OrchdLoginPolicyEmailList

Email white or black list for orchd login policy

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email_list** | **List[str]** |  | [optional] 

## Example

```python
from openapi_client.models.orchd_login_policy_email_list import OrchdLoginPolicyEmailList

# TODO update the JSON string below
json = "{}"
# create an instance of OrchdLoginPolicyEmailList from a JSON string
orchd_login_policy_email_list_instance = OrchdLoginPolicyEmailList.from_json(json)
# print the JSON string representation of the object
print(OrchdLoginPolicyEmailList.to_json())

# convert the object into a dict
orchd_login_policy_email_list_dict = orchd_login_policy_email_list_instance.to_dict()
# create an instance of OrchdLoginPolicyEmailList from a dict
orchd_login_policy_email_list_from_dict = OrchdLoginPolicyEmailList.from_dict(orchd_login_policy_email_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


