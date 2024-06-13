# RewriteChainRule


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**pattern** | **str** |  | 
**substitution** | **str** |  | 
**flags** | **List[str]** |  | 

## Example

```python
from openapi_client.models.rewrite_chain_rule import RewriteChainRule

# TODO update the JSON string below
json = "{}"
# create an instance of RewriteChainRule from a JSON string
rewrite_chain_rule_instance = RewriteChainRule.from_json(json)
# print the JSON string representation of the object
print(RewriteChainRule.to_json())

# convert the object into a dict
rewrite_chain_rule_dict = rewrite_chain_rule_instance.to_dict()
# create an instance of RewriteChainRule from a dict
rewrite_chain_rule_from_dict = RewriteChainRule.from_dict(rewrite_chain_rule_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


