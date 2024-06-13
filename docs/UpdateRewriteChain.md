# UpdateRewriteChain

If the `rule` property is missing, we will delete a rule on the given line number instead. If just the `conds` property is missing, it defauls to an empty array.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**line_number** | **float** |  | 
**rule** | [**RewriteChainRule**](RewriteChainRule.md) |  | [optional] 
**conds** | [**List[RewriteChainCondsInner]**](RewriteChainCondsInner.md) |  | [optional] 

## Example

```python
from openapi_client.models.update_rewrite_chain import UpdateRewriteChain

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateRewriteChain from a JSON string
update_rewrite_chain_instance = UpdateRewriteChain.from_json(json)
# print the JSON string representation of the object
print(UpdateRewriteChain.to_json())

# convert the object into a dict
update_rewrite_chain_dict = update_rewrite_chain_instance.to_dict()
# create an instance of UpdateRewriteChain from a dict
update_rewrite_chain_from_dict = UpdateRewriteChain.from_dict(update_rewrite_chain_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


