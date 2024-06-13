# DomainInUseStatus


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** |  | 
**website_id** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.domain_in_use_status import DomainInUseStatus

# TODO update the JSON string below
json = "{}"
# create an instance of DomainInUseStatus from a JSON string
domain_in_use_status_instance = DomainInUseStatus.from_json(json)
# print the JSON string representation of the object
print(DomainInUseStatus.to_json())

# convert the object into a dict
domain_in_use_status_dict = domain_in_use_status_instance.to_dict()
# create an instance of DomainInUseStatus from a dict
domain_in_use_status_from_dict = DomainInUseStatus.from_dict(domain_in_use_status_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


