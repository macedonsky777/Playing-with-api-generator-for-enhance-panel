# LogGreetingsMessageMetadata

The service has returned a payload we didn't expect. There's a chance of different service running at the standard port.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**greetings_message** | **str** | This is a list of bytes which have been returned by the service. For example \&quot;[50,50,48,32]\&quot;. | 

## Example

```python
from openapi_client.models.log_greetings_message_metadata import LogGreetingsMessageMetadata

# TODO update the JSON string below
json = "{}"
# create an instance of LogGreetingsMessageMetadata from a JSON string
log_greetings_message_metadata_instance = LogGreetingsMessageMetadata.from_json(json)
# print the JSON string representation of the object
print(LogGreetingsMessageMetadata.to_json())

# convert the object into a dict
log_greetings_message_metadata_dict = log_greetings_message_metadata_instance.to_dict()
# create an instance of LogGreetingsMessageMetadata from a dict
log_greetings_message_metadata_from_dict = LogGreetingsMessageMetadata.from_dict(log_greetings_message_metadata_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


