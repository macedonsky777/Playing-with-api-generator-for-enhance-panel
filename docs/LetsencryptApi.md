# openapi_client.LetsencryptApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_website_domain_letsencrypt_certs**](LetsencryptApi.md#create_website_domain_letsencrypt_certs) | **POST** /v2/domains/{domain_id}/letsencrypt | Generate and setup letsencrypt ssl certificates for website&#39;s domain
[**create_website_mail_domain_letsencrypt_certs**](LetsencryptApi.md#create_website_mail_domain_letsencrypt_certs) | **POST** /v2/domains/{domain_id}/letsencrypt_mail | Generate and setup letsencrypt ssl certificates for website&#39;s domain with mail. prefix.
[**perform_lets_encrypt_preflight_check**](LetsencryptApi.md#perform_lets_encrypt_preflight_check) | **POST** /v2/domains/{domain_id}/letsencrypt_preflight | Perform the LetsEncrypt preflight check


# **create_website_domain_letsencrypt_certs**
> create_website_domain_letsencrypt_certs(domain_id)

Generate and setup letsencrypt ssl certificates for website's domain

Generates letsencrypt certificates for the domain. This is a longer running task, that will do a complete ssl setup for a given domain. Once completed any given domain will get served over `https`. Given domain must be publicly accessible and being served from our service. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.LetsencryptApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Generate and setup letsencrypt ssl certificates for website's domain
        api_instance.create_website_domain_letsencrypt_certs(domain_id)
    except Exception as e:
        print("Exception when calling LetsencryptApi->create_website_domain_letsencrypt_certs: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | SSL Certs successfully created |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_website_mail_domain_letsencrypt_certs**
> create_website_mail_domain_letsencrypt_certs(domain_id)

Generate and setup letsencrypt ssl certificates for website's domain with mail. prefix.

Generates letsencrypt certificate for the mail server at mail.customerdomain.

### Example


```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.LetsencryptApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Generate and setup letsencrypt ssl certificates for website's domain with mail. prefix.
        api_instance.create_website_mail_domain_letsencrypt_certs(domain_id)
    except Exception as e:
        print("Exception when calling LetsencryptApi->create_website_mail_domain_letsencrypt_certs: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | SSL Certs successfully created |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **perform_lets_encrypt_preflight_check**
> LetsEncryptPreflightResult perform_lets_encrypt_preflight_check(domain_id)

Perform the LetsEncrypt preflight check

Will attempt to verify that the domain will successfully achieve a LetsEncrypt certificate if attempted.  Provides debug information.

### Example


```python
import openapi_client
from openapi_client.models.lets_encrypt_preflight_result import LetsEncryptPreflightResult
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.LetsencryptApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Perform the LetsEncrypt preflight check
        api_response = api_instance.perform_lets_encrypt_preflight_check(domain_id)
        print("The response of LetsencryptApi->perform_lets_encrypt_preflight_check:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LetsencryptApi->perform_lets_encrypt_preflight_check: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 

### Return type

[**LetsEncryptPreflightResult**](LetsEncryptPreflightResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Preflight check completed |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

