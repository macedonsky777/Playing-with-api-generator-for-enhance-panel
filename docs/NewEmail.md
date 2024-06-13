# NewEmail


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**mailbox_name** | **str** |  | [optional] 
**mailbox_password** | **str** |  | [optional] 
**username** | **str** |  | 
**aliases** | **List[str]** |  | [optional] 
**forwarders** | **List[str]** |  | [optional] 
**quota** | **int** |  | [optional] 

## Example

```python
from openapi_client.models.new_email import NewEmail

# TODO update the JSON string below
json = "{}"
# create an instance of NewEmail from a JSON string
new_email_instance = NewEmail.from_json(json)
# print the JSON string representation of the object
print(NewEmail.to_json())

# convert the object into a dict
new_email_dict = new_email_instance.to_dict()
# create an instance of NewEmail from a dict
new_email_from_dict = NewEmail.from_dict(new_email_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


