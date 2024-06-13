# NewSslCert


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cert** | **str** |  | 
**key** | **str** |  | 

## Example

```python
from openapi_client.models.new_ssl_cert import NewSslCert

# TODO update the JSON string below
json = "{}"
# create an instance of NewSslCert from a JSON string
new_ssl_cert_instance = NewSslCert.from_json(json)
# print the JSON string representation of the object
print(NewSslCert.to_json())

# convert the object into a dict
new_ssl_cert_dict = new_ssl_cert_instance.to_dict()
# create an instance of NewSslCert from a dict
new_ssl_cert_from_dict = NewSslCert.from_dict(new_ssl_cert_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


