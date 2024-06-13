# NewSshKey


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**value** | **str** | The SSH key in PEM format. | 
**name** | **str** | The friendly name associated with the key. | [optional] 

## Example

```python
from openapi_client.models.new_ssh_key import NewSshKey

# TODO update the JSON string below
json = "{}"
# create an instance of NewSshKey from a JSON string
new_ssh_key_instance = NewSshKey.from_json(json)
# print the JSON string representation of the object
print(NewSshKey.to_json())

# convert the object into a dict
new_ssh_key_dict = new_ssh_key_instance.to_dict()
# create an instance of NewSshKey from a dict
new_ssh_key_from_dict = NewSshKey.from_dict(new_ssh_key_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


