# LicenceInfo

Enhance Licence information with its status and key (if set)

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** |  | [optional] 
**status** | [**LicenceStatus**](LicenceStatus.md) |  | 

## Example

```python
from openapi_client.models.licence_info import LicenceInfo

# TODO update the JSON string below
json = "{}"
# create an instance of LicenceInfo from a JSON string
licence_info_instance = LicenceInfo.from_json(json)
# print the JSON string representation of the object
print(LicenceInfo.to_json())

# convert the object into a dict
licence_info_dict = licence_info_instance.to_dict()
# create an instance of LicenceInfo from a dict
licence_info_from_dict = LicenceInfo.from_dict(licence_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


