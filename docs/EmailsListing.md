# EmailsListing


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[Email]**](Email.md) |  | 
**total** | **int** |  | 

## Example

```python
from openapi_client.models.emails_listing import EmailsListing

# TODO update the JSON string below
json = "{}"
# create an instance of EmailsListing from a JSON string
emails_listing_instance = EmailsListing.from_json(json)
# print the JSON string representation of the object
print(EmailsListing.to_json())

# convert the object into a dict
emails_listing_dict = emails_listing_instance.to_dict()
# create an instance of EmailsListing from a dict
emails_listing_from_dict = EmailsListing.from_dict(emails_listing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


