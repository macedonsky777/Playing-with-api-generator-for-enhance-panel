# FtpUser


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**account** | **str** |  | 
**home_dir** | **str** | Homedir must be a relative path to the website&#39;s base dir. Set to empty string to use website base dir as FtpUser&#39;s home. | 
**website_id** | **str** |  | 

## Example

```python
from openapi_client.models.ftp_user import FtpUser

# TODO update the JSON string below
json = "{}"
# create an instance of FtpUser from a JSON string
ftp_user_instance = FtpUser.from_json(json)
# print the JSON string representation of the object
print(FtpUser.to_json())

# convert the object into a dict
ftp_user_dict = ftp_user_instance.to_dict()
# create an instance of FtpUser from a dict
ftp_user_from_dict = FtpUser.from_dict(ftp_user_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


