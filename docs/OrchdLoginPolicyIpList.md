# OrchdLoginPolicyIpList

Ip white or black list for orchd login policy

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ip_list** | **List[str]** |  | [optional] 

## Example

```python
from openapi_client.models.orchd_login_policy_ip_list import OrchdLoginPolicyIpList

# TODO update the JSON string below
json = "{}"
# create an instance of OrchdLoginPolicyIpList from a JSON string
orchd_login_policy_ip_list_instance = OrchdLoginPolicyIpList.from_json(json)
# print the JSON string representation of the object
print(OrchdLoginPolicyIpList.to_json())

# convert the object into a dict
orchd_login_policy_ip_list_dict = orchd_login_policy_ip_list_instance.to_dict()
# create an instance of OrchdLoginPolicyIpList from a dict
orchd_login_policy_ip_list_from_dict = OrchdLoginPolicyIpList.from_dict(orchd_login_policy_ip_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


