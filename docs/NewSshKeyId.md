# NewSshKeyId


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The unique ID of the SSH key within the same authorized_keys file. | 

## Example

```python
from openapi_client.models.new_ssh_key_id import NewSshKeyId

# TODO update the JSON string below
json = "{}"
# create an instance of NewSshKeyId from a JSON string
new_ssh_key_id_instance = NewSshKeyId.from_json(json)
# print the JSON string representation of the object
print(NewSshKeyId.to_json())

# convert the object into a dict
new_ssh_key_id_dict = new_ssh_key_id_instance.to_dict()
# create an instance of NewSshKeyId from a dict
new_ssh_key_id_from_dict = NewSshKeyId.from_dict(new_ssh_key_id_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


