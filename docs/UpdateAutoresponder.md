# UpdateAutoresponder


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**start_date** | **date** |  | [optional] 
**end_date** | **date** |  | [optional] 
**enabled** | **bool** |  | [optional] 
**subject** | **str** |  | [optional] 
**body** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.update_autoresponder import UpdateAutoresponder

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateAutoresponder from a JSON string
update_autoresponder_instance = UpdateAutoresponder.from_json(json)
# print the JSON string representation of the object
print(UpdateAutoresponder.to_json())

# convert the object into a dict
update_autoresponder_dict = update_autoresponder_instance.to_dict()
# create an instance of UpdateAutoresponder from a dict
update_autoresponder_from_dict = UpdateAutoresponder.from_dict(update_autoresponder_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


