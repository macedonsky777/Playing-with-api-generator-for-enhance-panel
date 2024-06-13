# NewFtpUser


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account** | **str** |  | 
**password** | **str** |  | 
**home_dir** | **str** |  | 

## Example

```python
from openapi_client.models.new_ftp_user import NewFtpUser

# TODO update the JSON string below
json = "{}"
# create an instance of NewFtpUser from a JSON string
new_ftp_user_instance = NewFtpUser.from_json(json)
# print the JSON string representation of the object
print(NewFtpUser.to_json())

# convert the object into a dict
new_ftp_user_dict = new_ftp_user_instance.to_dict()
# create an instance of NewFtpUser from a dict
new_ftp_user_from_dict = NewFtpUser.from_dict(new_ftp_user_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


