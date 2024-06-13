# SshKeyUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**value** | **str** | The SSH key in PEM format. | [optional] 
**name** | **str** | The friendly name associated with the key. | [optional] 

## Example

```python
from openapi_client.models.ssh_key_update import SshKeyUpdate

# TODO update the JSON string below
json = "{}"
# create an instance of SshKeyUpdate from a JSON string
ssh_key_update_instance = SshKeyUpdate.from_json(json)
# print the JSON string representation of the object
print(SshKeyUpdate.to_json())

# convert the object into a dict
ssh_key_update_dict = ssh_key_update_instance.to_dict()
# create an instance of SshKeyUpdate from a dict
ssh_key_update_from_dict = SshKeyUpdate.from_dict(ssh_key_update_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


