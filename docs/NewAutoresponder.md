# NewAutoresponder


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**start_date** | **date** |  | 
**end_date** | **date** |  | [optional] 
**enabled** | **bool** |  | 
**subject** | **str** |  | 
**body** | **str** |  | 

## Example

```python
from openapi_client.models.new_autoresponder import NewAutoresponder

# TODO update the JSON string below
json = "{}"
# create an instance of NewAutoresponder from a JSON string
new_autoresponder_instance = NewAutoresponder.from_json(json)
# print the JSON string representation of the object
print(NewAutoresponder.to_json())

# convert the object into a dict
new_autoresponder_dict = new_autoresponder_instance.to_dict()
# create an instance of NewAutoresponder from a dict
new_autoresponder_from_dict = NewAutoresponder.from_dict(new_autoresponder_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


