# openapi_client.DomainsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**check_domain**](DomainsApi.md#check_domain) | **POST** /orgs/{org_id}/domains/check | Check if a domain can be created
[**create_domain**](DomainsApi.md#create_domain) | **POST** /orgs/{org_id}/domains | Create domain
[**create_website_domain_letsencrypt_certs**](DomainsApi.md#create_website_domain_letsencrypt_certs) | **POST** /v2/domains/{domain_id}/letsencrypt | Generate and setup letsencrypt ssl certificates for website&#39;s domain
[**create_website_mail_domain_letsencrypt_certs**](DomainsApi.md#create_website_mail_domain_letsencrypt_certs) | **POST** /v2/domains/{domain_id}/letsencrypt_mail | Generate and setup letsencrypt ssl certificates for website&#39;s domain with mail. prefix.
[**create_website_mapped_domain**](DomainsApi.md#create_website_mapped_domain) | **POST** /orgs/{org_id}/websites/{website_id}/domains | Create website mapped domain
[**delete_cloudflare_api_key_id**](DomainsApi.md#delete_cloudflare_api_key_id) | **DELETE** /orgs/{org_id}/domains/{domain_id}/cloudflare | Delete CloudFlare API key, domain level
[**delete_domain**](DomainsApi.md#delete_domain) | **DELETE** /orgs/{org_id}/domains/{domain_id} | Delete domain
[**delete_website_domain_mapping**](DomainsApi.md#delete_website_domain_mapping) | **DELETE** /orgs/{org_id}/websites/{website_id}/domains/{domain_id} | Delete website domain mapping
[**delete_website_domain_vhost**](DomainsApi.md#delete_website_domain_vhost) | **DELETE** /v2/domains/{domain_id}/vhost | Deletes domain&#39;s custom vhost file if any
[**get_cloudflare_api_key_domain**](DomainsApi.md#get_cloudflare_api_key_domain) | **GET** /orgs/{org_id}/domains/{domain_id}/cloudflare | Get CloudFlare API key, domain level
[**get_cloudflare_name_servers**](DomainsApi.md#get_cloudflare_name_servers) | **GET** /orgs/{org_id}/domains/{domain_id}/cloudflare/nameservers | Get CloudFlare name servers
[**get_domain_auth_ns**](DomainsApi.md#get_domain_auth_ns) | **GET** /orgs/{org_id}/domains/{domain_id}/auth-ns | Get authoritative nameservers for domain.
[**get_domains**](DomainsApi.md#get_domains) | **GET** /orgs/{org_id}/domains | Get domains
[**get_website_domain_dns_query**](DomainsApi.md#get_website_domain_dns_query) | **GET** /orgs/{org_id}/websites/{website_id}/domains/{domain_id}/dns-query | Recursively query Dns servers for given domain
[**get_website_domain_mapping**](DomainsApi.md#get_website_domain_mapping) | **GET** /orgs/{org_id}/websites/{website_id}/domains/{domain_id} | Returns website domain mapping
[**get_website_domain_mapping_dns_status**](DomainsApi.md#get_website_domain_mapping_dns_status) | **GET** /orgs/{org_id}/websites/{website_id}/domains/{domain_id}/dns-status | Returns website domain mapping DNS status
[**get_website_domain_mappings**](DomainsApi.md#get_website_domain_mappings) | **GET** /orgs/{org_id}/websites/{website_id}/domains | Get website&#39;s mapped domains
[**get_website_domain_mod_sec_status**](DomainsApi.md#get_website_domain_mod_sec_status) | **GET** /v2/domains/{domain_id}/modsec_status | Get mod security status for a single domain
[**get_website_domain_vhost**](DomainsApi.md#get_website_domain_vhost) | **GET** /v2/domains/{domain_id}/vhost | Get domain&#39;s custom vhost file, if the file does not exist return empty string 
[**perform_lets_encrypt_preflight_check**](DomainsApi.md#perform_lets_encrypt_preflight_check) | **POST** /v2/domains/{domain_id}/letsencrypt_preflight | Perform the LetsEncrypt preflight check
[**set_cloudflare_api_key_id**](DomainsApi.md#set_cloudflare_api_key_id) | **PUT** /orgs/{org_id}/domains/{domain_id}/cloudflare | Set CloudFlare API key, domain level
[**set_website_domain_mod_sec_status**](DomainsApi.md#set_website_domain_mod_sec_status) | **PUT** /v2/domains/{domain_id}/modsec_status | Set mod security status on a single domain
[**set_website_domain_vhost**](DomainsApi.md#set_website_domain_vhost) | **PUT** /v2/domains/{domain_id}/vhost | Set a custom vhost file
[**update_website_domain_mapping**](DomainsApi.md#update_website_domain_mapping) | **PATCH** /orgs/{org_id}/websites/{website_id}/domains/{domain_id} | Update website domain mapping
[**update_website_primary_domain**](DomainsApi.md#update_website_primary_domain) | **PUT** /orgs/{org_id}/websites/{website_id}/domains/primary | Update primary domain mapping


# **check_domain**
> DomainInUseStatus check_domain(org_id, new_domain)

Check if a domain can be created

An organisation can perform a pre-flight check to see if a domain can be added.  This is useful for form validation.  It will return a status indicating if the domain is in use and, if so, whether it is on the current organisation or another.  If it is in use on the current organisation we will also return the websiteId the domain belongs to.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.domain_in_use_status import DomainInUseStatus
from openapi_client.models.new_domain import NewDomain
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DomainsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    new_domain = openapi_client.NewDomain() # NewDomain | Domain details.

    try:
        # Check if a domain can be created
        api_response = api_instance.check_domain(org_id, new_domain)
        print("The response of DomainsApi->check_domain:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DomainsApi->check_domain: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **new_domain** | [**NewDomain**](NewDomain.md)| Domain details. | 

### Return type

[**DomainInUseStatus**](DomainInUseStatus.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Domain in use status |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_domain**
> NewResourceUuid create_domain(org_id, new_domain)

Create domain

The MO may create domains without a subscription but all other customers need to pass with this request an id of one of their subscriptions to a plan that allows creating domain names.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_domain import NewDomain
from openapi_client.models.new_resource_uuid import NewResourceUuid
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DomainsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    new_domain = openapi_client.NewDomain() # NewDomain | Domain details.

    try:
        # Create domain
        api_response = api_instance.create_domain(org_id, new_domain)
        print("The response of DomainsApi->create_domain:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DomainsApi->create_domain: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **new_domain** | [**NewDomain**](NewDomain.md)| Domain details. | 

### Return type

[**NewResourceUuid**](NewResourceUuid.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Domain successfully created |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

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
    api_instance = openapi_client.DomainsApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Generate and setup letsencrypt ssl certificates for website's domain
        api_instance.create_website_domain_letsencrypt_certs(domain_id)
    except Exception as e:
        print("Exception when calling DomainsApi->create_website_domain_letsencrypt_certs: %s\n" % e)
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
    api_instance = openapi_client.DomainsApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Generate and setup letsencrypt ssl certificates for website's domain with mail. prefix.
        api_instance.create_website_mail_domain_letsencrypt_certs(domain_id)
    except Exception as e:
        print("Exception when calling DomainsApi->create_website_mail_domain_letsencrypt_certs: %s\n" % e)
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

# **create_website_mapped_domain**
> NewResourceUuid create_website_mapped_domain(org_id, website_id, new_mapped_domain)

Create website mapped domain

Creates a domain mapping, where subscription resources are sufficient. The mapping kind will default to 'alias' if unspecified.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_mapped_domain import NewMappedDomain
from openapi_client.models.new_resource_uuid import NewResourceUuid
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DomainsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    new_mapped_domain = openapi_client.NewMappedDomain() # NewMappedDomain | Domain details.

    try:
        # Create website mapped domain
        api_response = api_instance.create_website_mapped_domain(org_id, website_id, new_mapped_domain)
        print("The response of DomainsApi->create_website_mapped_domain:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DomainsApi->create_website_mapped_domain: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **new_mapped_domain** | [**NewMappedDomain**](NewMappedDomain.md)| Domain details. | 

### Return type

[**NewResourceUuid**](NewResourceUuid.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Successful |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_cloudflare_api_key_id**
> delete_cloudflare_api_key_id(org_id, domain_id)

Delete CloudFlare API key, domain level

Deletes the CloudFlare API key for a domain

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DomainsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Delete CloudFlare API key, domain level
        api_instance.delete_cloudflare_api_key_id(org_id, domain_id)
    except Exception as e:
        print("Exception when calling DomainsApi->delete_cloudflare_api_key_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **domain_id** | **str**| The id of the domain. | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | CloudFlare API key successfully deleted |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_domain**
> delete_domain(org_id, domain_id)

Delete domain

Deletes a domain. Only privileged org members or parent org admins may do this.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DomainsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Delete domain
        api_instance.delete_domain(org_id, domain_id)
    except Exception as e:
        print("Exception when calling DomainsApi->delete_domain: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **domain_id** | **str**| The id of the domain. | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Domain successfully deleted |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_website_domain_mapping**
> delete_website_domain_mapping(org_id, website_id, domain_id)

Delete website domain mapping

Deletes the domain mapping and decrements the domain alias quota usage in the website's subscription, if applicable. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DomainsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Delete website domain mapping
        api_instance.delete_website_domain_mapping(org_id, website_id, domain_id)
    except Exception as e:
        print("Exception when calling DomainsApi->delete_website_domain_mapping: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **domain_id** | **str**| The id of the domain. | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Website domain mapping successfully deleted |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_website_domain_vhost**
> delete_website_domain_vhost(domain_id, delete_website_domain_vhost_request)

Deletes domain's custom vhost file if any

### Example


```python
import openapi_client
from openapi_client.models.delete_website_domain_vhost_request import DeleteWebsiteDomainVhostRequest
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
    api_instance = openapi_client.DomainsApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.
    delete_website_domain_vhost_request = openapi_client.DeleteWebsiteDomainVhostRequest() # DeleteWebsiteDomainVhostRequest | 

    try:
        # Deletes domain's custom vhost file if any
        api_instance.delete_website_domain_vhost(domain_id, delete_website_domain_vhost_request)
    except Exception as e:
        print("Exception when calling DomainsApi->delete_website_domain_vhost: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 
 **delete_website_domain_vhost_request** | [**DeleteWebsiteDomainVhostRequest**](DeleteWebsiteDomainVhostRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Vhost deleted |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_cloudflare_api_key_domain**
> CloudFlareApiKey get_cloudflare_api_key_domain(org_id, domain_id)

Get CloudFlare API key, domain level

Returns the CloudFlare API key for a domain (obfuscated for security). This key will override an org level key.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.cloud_flare_api_key import CloudFlareApiKey
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DomainsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Get CloudFlare API key, domain level
        api_response = api_instance.get_cloudflare_api_key_domain(org_id, domain_id)
        print("The response of DomainsApi->get_cloudflare_api_key_domain:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DomainsApi->get_cloudflare_api_key_domain: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **domain_id** | **str**| The id of the domain. | 

### Return type

[**CloudFlareApiKey**](CloudFlareApiKey.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | CloudFlare API successfully queried |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_cloudflare_name_servers**
> CloudFlareNameServers get_cloudflare_name_servers(org_id, domain_id)

Get CloudFlare name servers

Returns the CloudFlare nameservers for a given domain, if it exists in CloudFlare.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.cloud_flare_name_servers import CloudFlareNameServers
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DomainsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Get CloudFlare name servers
        api_response = api_instance.get_cloudflare_name_servers(org_id, domain_id)
        print("The response of DomainsApi->get_cloudflare_name_servers:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DomainsApi->get_cloudflare_name_servers: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **domain_id** | **str**| The id of the domain. | 

### Return type

[**CloudFlareNameServers**](CloudFlareNameServers.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | CloudFlare API successfully queried |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_domain_auth_ns**
> AuthNsResponse get_domain_auth_ns(org_id, domain_id)

Get authoritative nameservers for domain.

Get authoritative nameservers for domain and check if they match known DNS IPs of the Enhance cluster

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.auth_ns_response import AuthNsResponse
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DomainsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Get authoritative nameservers for domain.
        api_response = api_instance.get_domain_auth_ns(org_id, domain_id)
        print("The response of DomainsApi->get_domain_auth_ns:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DomainsApi->get_domain_auth_ns: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **domain_id** | **str**| The id of the domain. | 

### Return type

[**AuthNsResponse**](AuthNsResponse.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Auth nameservers queried for domain |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_domains**
> DomainsListing get_domains(org_id, offset=offset, limit=limit, sort_by=sort_by, sort_order=sort_order)

Get domains

Lists the domains belonging to this organization.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.domains_listing import DomainsListing
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DomainsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    offset = 56 # int | The offset from which to return items. (optional)
    limit = 56 # int | The maximum number of items to return. (optional)
    sort_by = 'sort_by_example' # str | The field by which to sort. (optional)
    sort_order = 'sort_order_example' # str | The direction in which to sort. Possible values are 'asc' and 'desc', defaulting to 'asc'. (optional)

    try:
        # Get domains
        api_response = api_instance.get_domains(org_id, offset=offset, limit=limit, sort_by=sort_by, sort_order=sort_order)
        print("The response of DomainsApi->get_domains:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DomainsApi->get_domains: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **offset** | **int**| The offset from which to return items. | [optional] 
 **limit** | **int**| The maximum number of items to return. | [optional] 
 **sort_by** | **str**| The field by which to sort. | [optional] 
 **sort_order** | **str**| The direction in which to sort. Possible values are &#39;asc&#39; and &#39;desc&#39;, defaulting to &#39;asc&#39;. | [optional] 

### Return type

[**DomainsListing**](DomainsListing.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Domains successfully queried |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_domain_dns_query**
> DnsQueryOutcome get_website_domain_dns_query(org_id, website_id, domain_id, resolve_depth=resolve_depth)

Recursively query Dns servers for given domain

Returns details about the dns servers of given domain. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.dns_query_outcome import DnsQueryOutcome
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DomainsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    domain_id = 'domain_id_example' # str | The id of the domain.
    resolve_depth = 'resolve_depth_example' # str | DNS query resolve depth, defaults to `short` if not provided. `short` -> takes the shortest path to resolve domain IP. `detailed` -> queries and returns output from all found Authoritative name servers. `queryAllTldNs` -> queries and returns results from all TLD name servers (very expensive). (optional)

    try:
        # Recursively query Dns servers for given domain
        api_response = api_instance.get_website_domain_dns_query(org_id, website_id, domain_id, resolve_depth=resolve_depth)
        print("The response of DomainsApi->get_website_domain_dns_query:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DomainsApi->get_website_domain_dns_query: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **domain_id** | **str**| The id of the domain. | 
 **resolve_depth** | **str**| DNS query resolve depth, defaults to &#x60;short&#x60; if not provided. &#x60;short&#x60; -&gt; takes the shortest path to resolve domain IP. &#x60;detailed&#x60; -&gt; queries and returns output from all found Authoritative name servers. &#x60;queryAllTldNs&#x60; -&gt; queries and returns results from all TLD name servers (very expensive). | [optional] 

### Return type

[**DnsQueryOutcome**](DnsQueryOutcome.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Dns query outcome successfully returned |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_domain_mapping**
> DomainMapping get_website_domain_mapping(org_id, website_id, domain_id)

Returns website domain mapping

Returns a domain by its id that is mapped to this website. Requires login to have admin privileges in this org. Since only the MO can create standalone domains, session holder must be at least a `SuperAdmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.domain_mapping import DomainMapping
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DomainsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Returns website domain mapping
        api_response = api_instance.get_website_domain_mapping(org_id, website_id, domain_id)
        print("The response of DomainsApi->get_website_domain_mapping:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DomainsApi->get_website_domain_mapping: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **domain_id** | **str**| The id of the domain. | 

### Return type

[**DomainMapping**](DomainMapping.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_domain_mapping_dns_status**
> DnsStatus get_website_domain_mapping_dns_status(org_id, website_id, domain_id)

Returns website domain mapping DNS status

Returns an indication of whether the domain correctly resolves to the server this website is on.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.dns_status import DnsStatus
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DomainsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Returns website domain mapping DNS status
        api_response = api_instance.get_website_domain_mapping_dns_status(org_id, website_id, domain_id)
        print("The response of DomainsApi->get_website_domain_mapping_dns_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DomainsApi->get_website_domain_mapping_dns_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **domain_id** | **str**| The id of the domain. | 

### Return type

[**DnsStatus**](DnsStatus.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_domain_mappings**
> DomainMappingsFullListing get_website_domain_mappings(org_id, website_id, with_ssl=with_ssl)

Get website's mapped domains

Returns a list of domains that are mapped to this website. Requires login to have admin privileges in this org.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.domain_mappings_full_listing import DomainMappingsFullListing
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DomainsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    with_ssl = True # bool | If set to true, domains are returned with applicable ssl certificates. (optional)

    try:
        # Get website's mapped domains
        api_response = api_instance.get_website_domain_mappings(org_id, website_id, with_ssl=with_ssl)
        print("The response of DomainsApi->get_website_domain_mappings:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DomainsApi->get_website_domain_mappings: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **with_ssl** | **bool**| If set to true, domains are returned with applicable ssl certificates. | [optional] 

### Return type

[**DomainMappingsFullListing**](DomainMappingsFullListing.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_domain_mod_sec_status**
> ModSecStatus get_website_domain_mod_sec_status(domain_id)

Get mod security status for a single domain

### Example


```python
import openapi_client
from openapi_client.models.mod_sec_status import ModSecStatus
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
    api_instance = openapi_client.DomainsApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Get mod security status for a single domain
        api_response = api_instance.get_website_domain_mod_sec_status(domain_id)
        print("The response of DomainsApi->get_website_domain_mod_sec_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DomainsApi->get_website_domain_mod_sec_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 

### Return type

[**ModSecStatus**](ModSecStatus.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Modsec status queried |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_domain_vhost**
> Vhost get_website_domain_vhost(domain_id)

Get domain's custom vhost file, if the file does not exist return empty string 

### Example


```python
import openapi_client
from openapi_client.models.vhost import Vhost
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
    api_instance = openapi_client.DomainsApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Get domain's custom vhost file, if the file does not exist return empty string 
        api_response = api_instance.get_website_domain_vhost(domain_id)
        print("The response of DomainsApi->get_website_domain_vhost:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DomainsApi->get_website_domain_vhost: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 

### Return type

[**Vhost**](Vhost.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Vhost file queried |  -  |
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
    api_instance = openapi_client.DomainsApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Perform the LetsEncrypt preflight check
        api_response = api_instance.perform_lets_encrypt_preflight_check(domain_id)
        print("The response of DomainsApi->perform_lets_encrypt_preflight_check:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DomainsApi->perform_lets_encrypt_preflight_check: %s\n" % e)
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

# **set_cloudflare_api_key_id**
> set_cloudflare_api_key_id(org_id, domain_id, body)

Set CloudFlare API key, domain level

Sets the CloudFlare API key for a domain.  This key will override an org level key.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DomainsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    domain_id = 'domain_id_example' # str | The id of the domain.
    body = 'body_example' # str | Cloudflare API key ID.

    try:
        # Set CloudFlare API key, domain level
        api_instance.set_cloudflare_api_key_id(org_id, domain_id, body)
    except Exception as e:
        print("Exception when calling DomainsApi->set_cloudflare_api_key_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **domain_id** | **str**| The id of the domain. | 
 **body** | **str**| Cloudflare API key ID. | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | CloudFlare API key successfully set |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_website_domain_mod_sec_status**
> set_website_domain_mod_sec_status(domain_id, mod_sec_status)

Set mod security status on a single domain

### Example


```python
import openapi_client
from openapi_client.models.mod_sec_status import ModSecStatus
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
    api_instance = openapi_client.DomainsApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.
    mod_sec_status = openapi_client.ModSecStatus() # ModSecStatus | 

    try:
        # Set mod security status on a single domain
        api_instance.set_website_domain_mod_sec_status(domain_id, mod_sec_status)
    except Exception as e:
        print("Exception when calling DomainsApi->set_website_domain_mod_sec_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 
 **mod_sec_status** | [**ModSecStatus**](ModSecStatus.md)|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Modsec status updated |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_website_domain_vhost**
> set_website_domain_vhost(domain_id, vhost)

Set a custom vhost file

### Example


```python
import openapi_client
from openapi_client.models.vhost import Vhost
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
    api_instance = openapi_client.DomainsApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.
    vhost = openapi_client.Vhost() # Vhost | 

    try:
        # Set a custom vhost file
        api_instance.set_website_domain_vhost(domain_id, vhost)
    except Exception as e:
        print("Exception when calling DomainsApi->set_website_domain_vhost: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 
 **vhost** | [**Vhost**](Vhost.md)|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Vhost file updated |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_website_domain_mapping**
> update_website_domain_mapping(org_id, website_id, domain_id, domain_mapping_update)

Update website domain mapping

Partially updates the domain mapping. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.domain_mapping_update import DomainMappingUpdate
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DomainsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    domain_id = 'domain_id_example' # str | The id of the domain.
    domain_mapping_update = openapi_client.DomainMappingUpdate() # DomainMappingUpdate | 

    try:
        # Update website domain mapping
        api_instance.update_website_domain_mapping(org_id, website_id, domain_id, domain_mapping_update)
    except Exception as e:
        print("Exception when calling DomainsApi->update_website_domain_mapping: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **domain_id** | **str**| The id of the domain. | 
 **domain_mapping_update** | [**DomainMappingUpdate**](DomainMappingUpdate.md)|  | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Successful |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_website_primary_domain**
> update_website_primary_domain(org_id, website_id, new_primary_domain_mapping)

Update primary domain mapping

This operation can only be done by a logged in superadmin or owner of the organization or its parent organization(s). Domain and website has to belong to this organization.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_primary_domain_mapping import NewPrimaryDomainMapping
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: sessionCookie
configuration.api_key['sessionCookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['sessionCookie'] = 'Bearer'

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DomainsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    new_primary_domain_mapping = openapi_client.NewPrimaryDomainMapping() # NewPrimaryDomainMapping | Domain mapping details.

    try:
        # Update primary domain mapping
        api_instance.update_website_primary_domain(org_id, website_id, new_primary_domain_mapping)
    except Exception as e:
        print("Exception when calling DomainsApi->update_website_primary_domain: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **new_primary_domain_mapping** | [**NewPrimaryDomainMapping**](NewPrimaryDomainMapping.md)| Domain mapping details. | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successfully made domain the primary domain of website |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

