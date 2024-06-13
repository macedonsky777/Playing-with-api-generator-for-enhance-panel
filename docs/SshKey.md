# SshKey


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The unique ID of the SSH key within the same authorized_keys file. | 
**created_at** | **datetime** | The datetime of when this SSH key was created. | 
**value** | **str** | The SSH key (without the comment). | 
**name** | **str** | The friendly name associated with the key. | [optional] 

## Example

```python
from openapi_client.models.ssh_key import SshKey

# TODO update the JSON string below
json = "{}"
# create an instance of SshKey from a JSON string
ssh_key_instance = SshKey.from_json(json)
# print the JSON string representation of the object
print(SshKey.to_json())

# convert the object into a dict
ssh_key_dict = ssh_key_instance.to_dict()
# create an instance of SshKey from a dict
ssh_key_from_dict = SshKey.from_dict(ssh_key_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


