# OwaspVersion


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**current** | **str** |  | 
**available** | **str** |  | 

## Example

```python
from openapi_client.models.owasp_version import OwaspVersion

# TODO update the JSON string below
json = "{}"
# create an instance of OwaspVersion from a JSON string
owasp_version_instance = OwaspVersion.from_json(json)
# print the JSON string representation of the object
print(OwaspVersion.to_json())

# convert the object into a dict
owasp_version_dict = owasp_version_instance.to_dict()
# create an instance of OwaspVersion from a dict
owasp_version_from_dict = OwaspVersion.from_dict(owasp_version_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


