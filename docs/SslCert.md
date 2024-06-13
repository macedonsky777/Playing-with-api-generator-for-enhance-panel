# SslCert


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cert** | **str** |  | 
**key** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.ssl_cert import SslCert

# TODO update the JSON string below
json = "{}"
# create an instance of SslCert from a JSON string
ssl_cert_instance = SslCert.from_json(json)
# print the JSON string representation of the object
print(SslCert.to_json())

# convert the object into a dict
ssl_cert_dict = ssl_cert_instance.to_dict()
# create an instance of SslCert from a dict
ssl_cert_from_dict = SslCert.from_dict(ssl_cert_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


