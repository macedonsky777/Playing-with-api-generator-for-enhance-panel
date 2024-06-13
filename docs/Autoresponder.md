# Autoresponder


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**email_id** | **str** |  | 
**start_date** | **date** |  | 
**end_date** | **date** |  | [optional] 
**enabled** | **bool** |  | 
**subject** | **str** |  | 
**body** | **str** |  | 

## Example

```python
from openapi_client.models.autoresponder import Autoresponder

# TODO update the JSON string below
json = "{}"
# create an instance of Autoresponder from a JSON string
autoresponder_instance = Autoresponder.from_json(json)
# print the JSON string representation of the object
print(Autoresponder.to_json())

# convert the object into a dict
autoresponder_dict = autoresponder_instance.to_dict()
# create an instance of Autoresponder from a dict
autoresponder_from_dict = Autoresponder.from_dict(autoresponder_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


