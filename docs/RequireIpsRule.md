# RequireIpsRule


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**kind** | [**RequireIpsRuleKind**](RequireIpsRuleKind.md) |  | 
**ips** | **List[str]** |  | 

## Example

```python
from openapi_client.models.require_ips_rule import RequireIpsRule

# TODO update the JSON string below
json = "{}"
# create an instance of RequireIpsRule from a JSON string
require_ips_rule_instance = RequireIpsRule.from_json(json)
# print the JSON string representation of the object
print(RequireIpsRule.to_json())

# convert the object into a dict
require_ips_rule_dict = require_ips_rule_instance.to_dict()
# create an instance of RequireIpsRule from a dict
require_ips_rule_from_dict = RequireIpsRule.from_dict(require_ips_rule_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


