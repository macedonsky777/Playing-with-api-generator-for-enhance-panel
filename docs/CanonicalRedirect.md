# CanonicalRedirect

If this object is present, the website's .htaccess will have a new set of rules which redirect all secondary domains to this primary domain with 301 header. If this object is missing, any existing rules will be removed.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**use_www** | **bool** | Whether to put www to the url which is being redirected to. In .htaccess syntax: &#x60;http://www.example.com/$1&#x60; | 
**use_https** | **bool** | Whether to put www to the url which is being redirected to. In .htaccess syntax: &#x60;https://example.com/$1&#x60; | 

## Example

```python
from openapi_client.models.canonical_redirect import CanonicalRedirect

# TODO update the JSON string below
json = "{}"
# create an instance of CanonicalRedirect from a JSON string
canonical_redirect_instance = CanonicalRedirect.from_json(json)
# print the JSON string representation of the object
print(CanonicalRedirect.to_json())

# convert the object into a dict
canonical_redirect_dict = canonical_redirect_instance.to_dict()
# create an instance of CanonicalRedirect from a dict
canonical_redirect_from_dict = CanonicalRedirect.from_dict(canonical_redirect_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


