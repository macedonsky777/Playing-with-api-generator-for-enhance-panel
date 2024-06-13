# FtpUserUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**home_dir** | **str** | Homedir must be a relative path to the website&#39;s base dir. Set to empty string to use website base dir as FtpUser&#39;s home. | [optional] 
**password** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.ftp_user_update import FtpUserUpdate

# TODO update the JSON string below
json = "{}"
# create an instance of FtpUserUpdate from a JSON string
ftp_user_update_instance = FtpUserUpdate.from_json(json)
# print the JSON string representation of the object
print(FtpUserUpdate.to_json())

# convert the object into a dict
ftp_user_update_dict = ftp_user_update_instance.to_dict()
# create an instance of FtpUserUpdate from a dict
ftp_user_update_from_dict = FtpUserUpdate.from_dict(ftp_user_update_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


