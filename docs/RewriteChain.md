# RewriteChain


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**line_number** | **float** |  | 
**rule** | [**RewriteChainRule**](RewriteChainRule.md) |  | 
**conds** | [**List[RewriteChainCondsInner]**](RewriteChainCondsInner.md) |  | 

## Example

```python
from openapi_client.models.rewrite_chain import RewriteChain

# TODO update the JSON string below
json = "{}"
# create an instance of RewriteChain from a JSON string
rewrite_chain_instance = RewriteChain.from_json(json)
# print the JSON string representation of the object
print(RewriteChain.to_json())

# convert the object into a dict
rewrite_chain_dict = rewrite_chain_instance.to_dict()
# create an instance of RewriteChain from a dict
rewrite_chain_from_dict = RewriteChain.from_dict(rewrite_chain_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


