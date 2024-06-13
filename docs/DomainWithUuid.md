# DomainWithUuid


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain_id** | **str** |  | 
**domain_name** | **str** |  | 
**is_primary** | **bool** |  | 

## Example

```python
from openapi_client.models.domain_with_uuid import DomainWithUuid

# TODO update the JSON string below
json = "{}"
# create an instance of DomainWithUuid from a JSON string
domain_with_uuid_instance = DomainWithUuid.from_json(json)
# print the JSON string representation of the object
print(DomainWithUuid.to_json())

# convert the object into a dict
domain_with_uuid_dict = domain_with_uuid_instance.to_dict()
# create an instance of DomainWithUuid from a dict
domain_with_uuid_from_dict = DomainWithUuid.from_dict(domain_with_uuid_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


