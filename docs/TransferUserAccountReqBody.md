# TransferUserAccountReqBody


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subscription_id** | **int** |  | [optional] 
**allow_partial_sync** | **bool** |  | [optional] 
**app_server_id** | **str** |  | [optional] 
**backup_server_id** | **str** |  | [optional] 
**db_server_id** | **str** |  | [optional] 
**email_server_id** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.transfer_user_account_req_body import TransferUserAccountReqBody

# TODO update the JSON string below
json = "{}"
# create an instance of TransferUserAccountReqBody from a JSON string
transfer_user_account_req_body_instance = TransferUserAccountReqBody.from_json(json)
# print the JSON string representation of the object
print(TransferUserAccountReqBody.to_json())

# convert the object into a dict
transfer_user_account_req_body_dict = transfer_user_account_req_body_instance.to_dict()
# create an instance of TransferUserAccountReqBody from a dict
transfer_user_account_req_body_from_dict = TransferUserAccountReqBody.from_dict(transfer_user_account_req_body_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


