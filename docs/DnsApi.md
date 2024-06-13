# openapi_client.DnsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_default_dns_record**](DnsApi.md#create_default_dns_record) | **POST** /v2/settings/dns/default-records | Create a default DNS record
[**create_dns_third_party_provider**](DnsApi.md#create_dns_third_party_provider) | **POST** /dns/third-party-providers | Create new third party provider.
[**create_website_domain_dns_zone_record**](DnsApi.md#create_website_domain_dns_zone_record) | **POST** /orgs/{org_id}/websites/{website_id}/domains/{domain_id}/dns-zone/records | Create a new dns record for website domain
[**delete_default_dns_record**](DnsApi.md#delete_default_dns_record) | **DELETE** /v2/settings/dns/default-records/{record_id} | Delete a default DNS record
[**delete_dns_third_party_provider**](DnsApi.md#delete_dns_third_party_provider) | **DELETE** /dns/third-party-providers/{provider_id} | Deletes a third party dns provider.
[**delete_website_domain_dns_zone_record**](DnsApi.md#delete_website_domain_dns_zone_record) | **DELETE** /orgs/{org_id}/websites/{website_id}/domains/{domain_id}/dns-zone/records/{record_id} | Delete dns zone record
[**disable_domain_dns_sec**](DnsApi.md#disable_domain_dns_sec) | **DELETE** /orgs/{org_id}/websites/{website_id}/domains/{domain_id}/dns-zone/dnssec | Disable DNSSEC on this domain
[**enable_domain_dns_sec**](DnsApi.md#enable_domain_dns_sec) | **POST** /orgs/{org_id}/websites/{website_id}/domains/{domain_id}/dns-zone/dnssec | Enable DNSSEC on this domain
[**get_dns_third_party_providers**](DnsApi.md#get_dns_third_party_providers) | **GET** /dns/third-party-providers | Lists all third party providers.
[**get_website_domain_dns_zone**](DnsApi.md#get_website_domain_dns_zone) | **GET** /orgs/{org_id}/websites/{website_id}/domains/{domain_id}/dns-zone | Get a dns zone for given domain
[**list_default_dns_records**](DnsApi.md#list_default_dns_records) | **GET** /v2/settings/dns/default-records | List default DNS records
[**update_default_dns_record**](DnsApi.md#update_default_dns_record) | **PATCH** /v2/settings/dns/default-records/{record_id} | Update a default DNS record
[**update_website_domain_dns_zone**](DnsApi.md#update_website_domain_dns_zone) | **PATCH** /orgs/{org_id}/websites/{website_id}/domains/{domain_id}/dns-zone | Updates a dns zone SOA for website domain
[**update_website_domain_dns_zone_record**](DnsApi.md#update_website_domain_dns_zone_record) | **PATCH** /orgs/{org_id}/websites/{website_id}/domains/{domain_id}/dns-zone/records/{record_id} | Updates a dns record for given domain


# **create_default_dns_record**
> str create_default_dns_record(new_default_dns_record)

Create a default DNS record

Creates a default record at a platform level which will be added to all newly created DNS zones.  In the value you can use $$origin$$ which will be substituted for the origin domain.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_default_dns_record import NewDefaultDnsRecord
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
    api_instance = openapi_client.DnsApi(api_client)
    new_default_dns_record = openapi_client.NewDefaultDnsRecord() # NewDefaultDnsRecord | 

    try:
        # Create a default DNS record
        api_response = api_instance.create_default_dns_record(new_default_dns_record)
        print("The response of DnsApi->create_default_dns_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DnsApi->create_default_dns_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **new_default_dns_record** | [**NewDefaultDnsRecord**](NewDefaultDnsRecord.md)|  | 

### Return type

**str**

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Created |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_dns_third_party_provider**
> create_dns_third_party_provider(new_dns_third_party_provider)

Create new third party provider.

This operation can only be done by an MO admin. Third party providers are notified about changes to dns zones within Enhance. This endpoint creates a new provider which is going to be notified on provided URL about dns updates. Please not that after adding a new provider using this endpoint, the provider will initially receive a request to delete all its current data and then Enhance will send a request with all existing dns zones.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_dns_third_party_provider import NewDnsThirdPartyProvider
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
    api_instance = openapi_client.DnsApi(api_client)
    new_dns_third_party_provider = openapi_client.NewDnsThirdPartyProvider() # NewDnsThirdPartyProvider | Url where the updates are sent and map of header names to their values.

    try:
        # Create new third party provider.
        api_instance.create_dns_third_party_provider(new_dns_third_party_provider)
    except Exception as e:
        print("Exception when calling DnsApi->create_dns_third_party_provider: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **new_dns_third_party_provider** | [**NewDnsThirdPartyProvider**](NewDnsThirdPartyProvider.md)| Url where the updates are sent and map of header names to their values. | 

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
**200** | Successful |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_website_domain_dns_zone_record**
> NewResourceUuid create_website_domain_dns_zone_record(org_id, website_id, domain_id, new_dns_record)

Create a new dns record for website domain

Creates a new dns record for a website's domain dns zone. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_dns_record import NewDnsRecord
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
    api_instance = openapi_client.DnsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    domain_id = 'domain_id_example' # str | The id of the domain.
    new_dns_record = openapi_client.NewDnsRecord() # NewDnsRecord | New dns record details.

    try:
        # Create a new dns record for website domain
        api_response = api_instance.create_website_domain_dns_zone_record(org_id, website_id, domain_id, new_dns_record)
        print("The response of DnsApi->create_website_domain_dns_zone_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DnsApi->create_website_domain_dns_zone_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **domain_id** | **str**| The id of the domain. | 
 **new_dns_record** | [**NewDnsRecord**](NewDnsRecord.md)| New dns record details. | 

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
**201** | Record successfully created |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_default_dns_record**
> delete_default_dns_record(record_id)

Delete a default DNS record

Delete a default DNS record.  Will not remove from existing zones.

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
    api_instance = openapi_client.DnsApi(api_client)
    record_id = 'record_id_example' # str | 

    try:
        # Delete a default DNS record
        api_instance.delete_default_dns_record(record_id)
    except Exception as e:
        print("Exception when calling DnsApi->delete_default_dns_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **record_id** | **str**|  | 

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
**200** | Deleted |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_dns_third_party_provider**
> delete_dns_third_party_provider(provider_id)

Deletes a third party dns provider.

This operation can only be done by an MO admin. Third party providers are notified about changes to dns zones within Enhance. This endpoint removes an existing provider. After this endpoint resolves, no new dns zones are going to be replicated to the provider.

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
    api_instance = openapi_client.DnsApi(api_client)
    provider_id = 56 # int | The id of the third party provider which can be obtained by querying the GET /dns/third-party-providers endpoint.

    try:
        # Deletes a third party dns provider.
        api_instance.delete_dns_third_party_provider(provider_id)
    except Exception as e:
        print("Exception when calling DnsApi->delete_dns_third_party_provider: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **provider_id** | **int**| The id of the third party provider which can be obtained by querying the GET /dns/third-party-providers endpoint. | 

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
**200** | Successful |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_website_domain_dns_zone_record**
> delete_website_domain_dns_zone_record(org_id, website_id, domain_id, record_id)

Delete dns zone record

Deletes a dns zone record for given domain. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

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
    api_instance = openapi_client.DnsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    domain_id = 'domain_id_example' # str | The id of the domain.
    record_id = 'record_id_example' # str | The id of the record.

    try:
        # Delete dns zone record
        api_instance.delete_website_domain_dns_zone_record(org_id, website_id, domain_id, record_id)
    except Exception as e:
        print("Exception when calling DnsApi->delete_website_domain_dns_zone_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **domain_id** | **str**| The id of the domain. | 
 **record_id** | **str**| The id of the record. | 

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
**204** | Record successfully deleted |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **disable_domain_dns_sec**
> disable_domain_dns_sec(org_id, website_id, domain_id)

Disable DNSSEC on this domain

Will disable DNSSEC on this domain.  The DS records must be removed from the upstream DNS provider first to avoid downtime.

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
    api_instance = openapi_client.DnsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Disable DNSSEC on this domain
        api_instance.disable_domain_dns_sec(org_id, website_id, domain_id)
    except Exception as e:
        print("Exception when calling DnsApi->disable_domain_dns_sec: %s\n" % e)
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
**200** | DNSSEC disabled |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **enable_domain_dns_sec**
> str enable_domain_dns_sec(org_id, website_id, domain_id)

Enable DNSSEC on this domain

Will enable DNSSEC and return the relevant DS records

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
    api_instance = openapi_client.DnsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Enable DNSSEC on this domain
        api_response = api_instance.enable_domain_dns_sec(org_id, website_id, domain_id)
        print("The response of DnsApi->enable_domain_dns_sec:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DnsApi->enable_domain_dns_sec: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **domain_id** | **str**| The id of the domain. | 

### Return type

**str**

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | DNSSEC enabled |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_dns_third_party_providers**
> List[DnsThirdPartyProvider] get_dns_third_party_providers()

Lists all third party providers.

This operation can only be done by an MO admin. Third party providers are notified about changes to dns zones within Enhance. This endpoint lists all registered URLs which listen to these changes.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.dns_third_party_provider import DnsThirdPartyProvider
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
    api_instance = openapi_client.DnsApi(api_client)

    try:
        # Lists all third party providers.
        api_response = api_instance.get_dns_third_party_providers()
        print("The response of DnsApi->get_dns_third_party_providers:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DnsApi->get_dns_third_party_providers: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**List[DnsThirdPartyProvider]**](DnsThirdPartyProvider.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_domain_dns_zone**
> DnsZone get_website_domain_dns_zone(org_id, website_id, domain_id)

Get a dns zone for given domain

Returns details about the dns zone of given domain. Returns Soa record and all other records. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.dns_zone import DnsZone
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
    api_instance = openapi_client.DnsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Get a dns zone for given domain
        api_response = api_instance.get_website_domain_dns_zone(org_id, website_id, domain_id)
        print("The response of DnsApi->get_website_domain_dns_zone:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DnsApi->get_website_domain_dns_zone: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **domain_id** | **str**| The id of the domain. | 

### Return type

[**DnsZone**](DnsZone.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Dns zone successfully returned |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_default_dns_records**
> List[DefaultDnsRecord] list_default_dns_records()

List default DNS records

Lists the DNS records which will be added to all newly created DNS zones.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.default_dns_record import DefaultDnsRecord
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
    api_instance = openapi_client.DnsApi(api_client)

    try:
        # List default DNS records
        api_response = api_instance.list_default_dns_records()
        print("The response of DnsApi->list_default_dns_records:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DnsApi->list_default_dns_records: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**List[DefaultDnsRecord]**](DefaultDnsRecord.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successfully listed |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_default_dns_record**
> update_default_dns_record(record_id, update_default_dns_record)

Update a default DNS record

Updates a default DNS record, all fields are optional.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.update_default_dns_record import UpdateDefaultDnsRecord
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
    api_instance = openapi_client.DnsApi(api_client)
    record_id = 'record_id_example' # str | 
    update_default_dns_record = openapi_client.UpdateDefaultDnsRecord() # UpdateDefaultDnsRecord | 

    try:
        # Update a default DNS record
        api_instance.update_default_dns_record(record_id, update_default_dns_record)
    except Exception as e:
        print("Exception when calling DnsApi->update_default_dns_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **record_id** | **str**|  | 
 **update_default_dns_record** | [**UpdateDefaultDnsRecord**](UpdateDefaultDnsRecord.md)|  | 

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
**200** | Updated |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_website_domain_dns_zone**
> update_website_domain_dns_zone(org_id, website_id, domain_id, update_dns_zone)

Updates a dns zone SOA for website domain

Partially updates dns zone SOA record for existing zone. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.update_dns_zone import UpdateDnsZone
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
    api_instance = openapi_client.DnsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    domain_id = 'domain_id_example' # str | The id of the domain.
    update_dns_zone = openapi_client.UpdateDnsZone() # UpdateDnsZone | Fields to update.

    try:
        # Updates a dns zone SOA for website domain
        api_instance.update_website_domain_dns_zone(org_id, website_id, domain_id, update_dns_zone)
    except Exception as e:
        print("Exception when calling DnsApi->update_website_domain_dns_zone: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **domain_id** | **str**| The id of the domain. | 
 **update_dns_zone** | [**UpdateDnsZone**](UpdateDnsZone.md)| Fields to update. | 

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
**204** | Zone successfully updated |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_website_domain_dns_zone_record**
> update_website_domain_dns_zone_record(org_id, website_id, domain_id, record_id, update_dns_record)

Updates a dns record for given domain

Partially updates a dns record for existing zone. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.update_dns_record import UpdateDnsRecord
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
    api_instance = openapi_client.DnsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    domain_id = 'domain_id_example' # str | The id of the domain.
    record_id = 'record_id_example' # str | The id of the record.
    update_dns_record = openapi_client.UpdateDnsRecord() # UpdateDnsRecord | Fields to update.

    try:
        # Updates a dns record for given domain
        api_instance.update_website_domain_dns_zone_record(org_id, website_id, domain_id, record_id, update_dns_record)
    except Exception as e:
        print("Exception when calling DnsApi->update_website_domain_dns_zone_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **domain_id** | **str**| The id of the domain. | 
 **record_id** | **str**| The id of the record. | 
 **update_dns_record** | [**UpdateDnsRecord**](UpdateDnsRecord.md)| Fields to update. | 

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
**204** | Record successfully updated |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

