# openapi_client.EmailsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_website_email**](EmailsApi.md#create_website_email) | **POST** /orgs/{org_id}/websites/{website_id}/domains/{domain_id}/emails | Create an email under website&#39;s domain
[**create_website_email_autoresponder**](EmailsApi.md#create_website_email_autoresponder) | **POST** /orgs/{org_id}/websites/{website_id}/emails/{email_id}/autoresponders | Create new website email autoresponder
[**delete_website_email**](EmailsApi.md#delete_website_email) | **DELETE** /orgs/{org_id}/websites/{website_id}/emails/{email_id} | Delete website email
[**delete_website_email_autoresponder**](EmailsApi.md#delete_website_email_autoresponder) | **DELETE** /orgs/{org_id}/websites/{website_id}/emails/{email_id}/autoresponders/{autoresponder_id} | Delete website email autoresponder
[**get_domain_email_auth**](EmailsApi.md#get_domain_email_auth) | **GET** /orgs/{org_id}/domains/{domain_id}/email-auth | Get email authentication preferences
[**get_domain_local_remote**](EmailsApi.md#get_domain_local_remote) | **GET** /orgs/{org_id}/websites/{website_id}/domains/{domain_id}/local_remote | Get the current local/remote status
[**get_emails**](EmailsApi.md#get_emails) | **GET** /orgs/{org_id}/emails | Get org emails
[**get_website_email**](EmailsApi.md#get_website_email) | **GET** /orgs/{org_id}/websites/{website_id}/emails/{email_id} | Get website email
[**get_website_email_autoresponders**](EmailsApi.md#get_website_email_autoresponders) | **GET** /orgs/{org_id}/websites/{website_id}/emails/{email_id}/autoresponders | Get website email autoresponders
[**get_website_email_client_conf**](EmailsApi.md#get_website_email_client_conf) | **GET** /orgs/{org_id}/websites/{website_id}/emails/{email_id}/client-conf | Get website email client configuration
[**get_website_emails**](EmailsApi.md#get_website_emails) | **GET** /orgs/{org_id}/websites/{website_id}/emails | Get website emails
[**set_domain_local_remote**](EmailsApi.md#set_domain_local_remote) | **PUT** /orgs/{org_id}/websites/{website_id}/domains/{domain_id}/local_remote | Update email local/remote status
[**update_domain_email_auth**](EmailsApi.md#update_domain_email_auth) | **PUT** /orgs/{org_id}/domains/{domain_id}/email-auth | Update email authentication preferences
[**update_website_email**](EmailsApi.md#update_website_email) | **PATCH** /orgs/{org_id}/websites/{website_id}/emails/{email_id} | Update website email
[**update_website_email_autoresponder**](EmailsApi.md#update_website_email_autoresponder) | **PATCH** /orgs/{org_id}/websites/{website_id}/emails/{email_id}/autoresponders/{autoresponder_id} | Update website email autoresponder
[**validate_domain_email_auth**](EmailsApi.md#validate_domain_email_auth) | **GET** /orgs/{org_id}/domains/{domain_id}/email-auth/validate | Validate email authentication DNS records


# **create_website_email**
> NewResourceUuid create_website_email(org_id, website_id, domain_id, new_email)

Create an email under website's domain

Creates a new email under the given website. The email may have a mailbox or it may be a forwarder, which means it merely serves to forward incoming emails to the specified email addresses. If a password is supplied, a mailbox is created. Otherwise, forwarders must be specified as an email must always have a delivery route. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.new_email import NewEmail
from openapi_client.models.new_resource_uuid import NewResourceUuid
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
    api_instance = openapi_client.EmailsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    domain_id = 'domain_id_example' # str | The id of the domain.
    new_email = openapi_client.NewEmail() # NewEmail | New email details.

    try:
        # Create an email under website's domain
        api_response = api_instance.create_website_email(org_id, website_id, domain_id, new_email)
        print("The response of EmailsApi->create_website_email:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmailsApi->create_website_email: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **domain_id** | **str**| The id of the domain. | 
 **new_email** | [**NewEmail**](NewEmail.md)| New email details. | 

### Return type

[**NewResourceUuid**](NewResourceUuid.md)

### Authorization

No authorization required

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

# **create_website_email_autoresponder**
> NewResourceId create_website_email_autoresponder(org_id, website_id, email_id, new_autoresponder)

Create new website email autoresponder

Creates a new autoresponder for the given email. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_autoresponder import NewAutoresponder
from openapi_client.models.new_resource_id import NewResourceId
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
    api_instance = openapi_client.EmailsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    email_id = 'email_id_example' # str | The id of the email.
    new_autoresponder = openapi_client.NewAutoresponder() # NewAutoresponder | Autoresponder details.

    try:
        # Create new website email autoresponder
        api_response = api_instance.create_website_email_autoresponder(org_id, website_id, email_id, new_autoresponder)
        print("The response of EmailsApi->create_website_email_autoresponder:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmailsApi->create_website_email_autoresponder: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **email_id** | **str**| The id of the email. | 
 **new_autoresponder** | [**NewAutoresponder**](NewAutoresponder.md)| Autoresponder details. | 

### Return type

[**NewResourceId**](NewResourceId.md)

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

# **delete_website_email**
> delete_website_email(org_id, website_id, email_id)

Delete website email

Deletes the email belonging to the given website. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

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
    api_instance = openapi_client.EmailsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    email_id = 'email_id_example' # str | The id of the email.

    try:
        # Delete website email
        api_instance.delete_website_email(org_id, website_id, email_id)
    except Exception as e:
        print("Exception when calling EmailsApi->delete_website_email: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **email_id** | **str**| The id of the email. | 

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
**204** | Email successfully deleted |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_website_email_autoresponder**
> delete_website_email_autoresponder(org_id, website_id, email_id, autoresponder_id)

Delete website email autoresponder

Deletes the autoresponder belonging to the given website email. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

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
    api_instance = openapi_client.EmailsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    email_id = 'email_id_example' # str | The id of the email.
    autoresponder_id = 56 # int | The id of the autoresponder.

    try:
        # Delete website email autoresponder
        api_instance.delete_website_email_autoresponder(org_id, website_id, email_id, autoresponder_id)
    except Exception as e:
        print("Exception when calling EmailsApi->delete_website_email_autoresponder: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **email_id** | **str**| The id of the email. | 
 **autoresponder_id** | **int**| The id of the autoresponder. | 

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
**204** | Autoresponder successfully deleted |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_domain_email_auth**
> EmailAuth get_domain_email_auth(org_id, domain_id)

Get email authentication preferences

Fetch DKIM setting for the mailboxes on a given domain.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.email_auth import EmailAuth
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
    api_instance = openapi_client.EmailsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Get email authentication preferences
        api_response = api_instance.get_domain_email_auth(org_id, domain_id)
        print("The response of EmailsApi->get_domain_email_auth:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmailsApi->get_domain_email_auth: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **domain_id** | **str**| The id of the domain. | 

### Return type

[**EmailAuth**](EmailAuth.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Email auth settings successfully queried |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_domain_local_remote**
> LocalRemoteBody get_domain_local_remote(org_id, website_id, domain_id)

Get the current local/remote status

Fetches the current status of the domain, whether it is treated as local or remote by the MTA

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.local_remote_body import LocalRemoteBody
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
    api_instance = openapi_client.EmailsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Get the current local/remote status
        api_response = api_instance.get_domain_local_remote(org_id, website_id, domain_id)
        print("The response of EmailsApi->get_domain_local_remote:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmailsApi->get_domain_local_remote: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **domain_id** | **str**| The id of the domain. | 

### Return type

[**LocalRemoteBody**](LocalRemoteBody.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Local remote status successfully queried |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_emails**
> EmailsListing get_emails(org_id, offset=offset, limit=limit, sort_by=sort_by, sort_order=sort_order, search=search, recursive=recursive, max_depth=max_depth, status=status, domain_id=domain_id, plan_id=plan_id, subscription_id=subscription_id, include_internal=include_internal, show_deleted=show_deleted)

Get org emails

Returns all emails belonging to this organization. Session holder must be at least a `SuperAdmin` in this org or a parent org.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.emails_listing import EmailsListing
from openapi_client.models.website_status import WebsiteStatus
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
    api_instance = openapi_client.EmailsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    offset = 56 # int | The offset from which to return items. (optional)
    limit = 56 # int | The maximum number of items to return. (optional)
    sort_by = 'sort_by_example' # str | The field by which to sort. (optional)
    sort_order = 'sort_order_example' # str | The direction in which to sort. Possible values are 'asc' and 'desc', defaulting to 'asc'. (optional)
    search = 'search_example' # str | Limit the result set to the resources whose names, partially and case insensitively, match the specified search term. E.g. for websites, this is their domain or tag, for databases the database name, for emails the email address or mailbox name, etc. A website will also be returned if the search term exactly matches the website's uuid. (optional)
    recursive = True # bool | If set to true, the endpoint will return resources in some hierarchy recursively, that is, several or all levels of the hierarchy, depending on whether `maxDepth` is set. E.g. for customers this means direct and indirect customers are returned. For websites, this returns websites of all direct and indirect customers. (optional)
    max_depth = 56 # int | If recursive is set to true, this can be specified to limit the recursion depth. By default there is no recursion bound. (optional)
    status = openapi_client.WebsiteStatus() # WebsiteStatus | Limit the result set to emails with the specified status. Only applicable if `recursive` is set to true. (optional)
    domain_id = 'domain_id_example' # str | Limit the result set to emails under domain. (optional)
    plan_id = 56 # int | Limit the result set to resources under subscriptions to the plan. (optional)
    subscription_id = 56 # int | Limit the result set to resources under subscription. (optional)
    include_internal = False # bool | Include internal emails in response (optional) (default to False)
    show_deleted = True # bool | Filters out deleted emails, which are otherwise returned in the result. Defaults to `showDeleted=true` if not set. Can only be set by MO, if set by others, a 403 is returned. (optional)

    try:
        # Get org emails
        api_response = api_instance.get_emails(org_id, offset=offset, limit=limit, sort_by=sort_by, sort_order=sort_order, search=search, recursive=recursive, max_depth=max_depth, status=status, domain_id=domain_id, plan_id=plan_id, subscription_id=subscription_id, include_internal=include_internal, show_deleted=show_deleted)
        print("The response of EmailsApi->get_emails:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmailsApi->get_emails: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **offset** | **int**| The offset from which to return items. | [optional] 
 **limit** | **int**| The maximum number of items to return. | [optional] 
 **sort_by** | **str**| The field by which to sort. | [optional] 
 **sort_order** | **str**| The direction in which to sort. Possible values are &#39;asc&#39; and &#39;desc&#39;, defaulting to &#39;asc&#39;. | [optional] 
 **search** | **str**| Limit the result set to the resources whose names, partially and case insensitively, match the specified search term. E.g. for websites, this is their domain or tag, for databases the database name, for emails the email address or mailbox name, etc. A website will also be returned if the search term exactly matches the website&#39;s uuid. | [optional] 
 **recursive** | **bool**| If set to true, the endpoint will return resources in some hierarchy recursively, that is, several or all levels of the hierarchy, depending on whether &#x60;maxDepth&#x60; is set. E.g. for customers this means direct and indirect customers are returned. For websites, this returns websites of all direct and indirect customers. | [optional] 
 **max_depth** | **int**| If recursive is set to true, this can be specified to limit the recursion depth. By default there is no recursion bound. | [optional] 
 **status** | [**WebsiteStatus**](.md)| Limit the result set to emails with the specified status. Only applicable if &#x60;recursive&#x60; is set to true. | [optional] 
 **domain_id** | **str**| Limit the result set to emails under domain. | [optional] 
 **plan_id** | **int**| Limit the result set to resources under subscriptions to the plan. | [optional] 
 **subscription_id** | **int**| Limit the result set to resources under subscription. | [optional] 
 **include_internal** | **bool**| Include internal emails in response | [optional] [default to False]
 **show_deleted** | **bool**| Filters out deleted emails, which are otherwise returned in the result. Defaults to &#x60;showDeleted&#x3D;true&#x60; if not set. Can only be set by MO, if set by others, a 403 is returned. | [optional] 

### Return type

[**EmailsListing**](EmailsListing.md)

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

# **get_website_email**
> EmailDetailed get_website_email(org_id, website_id, email_id)

Get website email

Returns details about the given email belonging to the given website. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.email_detailed import EmailDetailed
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
    api_instance = openapi_client.EmailsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    email_id = 'email_id_example' # str | The id of the email.

    try:
        # Get website email
        api_response = api_instance.get_website_email(org_id, website_id, email_id)
        print("The response of EmailsApi->get_website_email:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmailsApi->get_website_email: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **email_id** | **str**| The id of the email. | 

### Return type

[**EmailDetailed**](EmailDetailed.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Email successfully queried |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_email_autoresponders**
> AutorespondersFullListing get_website_email_autoresponders(org_id, website_id, email_id)

Get website email autoresponders

Returns autoresponders configured for the given email. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.autoresponders_full_listing import AutorespondersFullListing
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
    api_instance = openapi_client.EmailsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    email_id = 'email_id_example' # str | The id of the email.

    try:
        # Get website email autoresponders
        api_response = api_instance.get_website_email_autoresponders(org_id, website_id, email_id)
        print("The response of EmailsApi->get_website_email_autoresponders:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmailsApi->get_website_email_autoresponders: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **email_id** | **str**| The id of the email. | 

### Return type

[**AutorespondersFullListing**](AutorespondersFullListing.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Autoresponders successfully queried |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_email_client_conf**
> object get_website_email_client_conf(org_id, website_id, email_id)

Get website email client configuration

Returns the client configuration for the given email. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

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
    api_instance = openapi_client.EmailsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    email_id = 'email_id_example' # str | The id of the email.

    try:
        # Get website email client configuration
        api_response = api_instance.get_website_email_client_conf(org_id, website_id, email_id)
        print("The response of EmailsApi->get_website_email_client_conf:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmailsApi->get_website_email_client_conf: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **email_id** | **str**| The id of the email. | 

### Return type

**object**

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Email client config successfully queried |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_emails**
> EmailsListing get_website_emails(org_id, website_id, offset=offset, limit=limit, sort_by=sort_by, sort_order=sort_order, search=search, include_internal=include_internal)

Get website emails

Returns all emails belonging to a website. The results may optionally be sorted and paginated. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.emails_listing import EmailsListing
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
    api_instance = openapi_client.EmailsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    offset = 56 # int | The offset from which to return items. (optional)
    limit = 56 # int | The maximum number of items to return. (optional)
    sort_by = 'sort_by_example' # str | The field by which to sort. (optional)
    sort_order = 'sort_order_example' # str | The direction in which to sort. Possible values are 'asc' and 'desc', defaulting to 'asc'. (optional)
    search = 'search_example' # str | Limit the result set to the resources whose names, partially and case insensitively, match the specified search term. E.g. for websites, this is their domain or tag, for databases the database name, for emails the email address or mailbox name, etc. A website will also be returned if the search term exactly matches the website's uuid. (optional)
    include_internal = False # bool | Include internal emails in response (optional) (default to False)

    try:
        # Get website emails
        api_response = api_instance.get_website_emails(org_id, website_id, offset=offset, limit=limit, sort_by=sort_by, sort_order=sort_order, search=search, include_internal=include_internal)
        print("The response of EmailsApi->get_website_emails:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmailsApi->get_website_emails: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **offset** | **int**| The offset from which to return items. | [optional] 
 **limit** | **int**| The maximum number of items to return. | [optional] 
 **sort_by** | **str**| The field by which to sort. | [optional] 
 **sort_order** | **str**| The direction in which to sort. Possible values are &#39;asc&#39; and &#39;desc&#39;, defaulting to &#39;asc&#39;. | [optional] 
 **search** | **str**| Limit the result set to the resources whose names, partially and case insensitively, match the specified search term. E.g. for websites, this is their domain or tag, for databases the database name, for emails the email address or mailbox name, etc. A website will also be returned if the search term exactly matches the website&#39;s uuid. | [optional] 
 **include_internal** | **bool**| Include internal emails in response | [optional] [default to False]

### Return type

[**EmailsListing**](EmailsListing.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Emails successfully queried |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_domain_local_remote**
> set_domain_local_remote(org_id, website_id, domain_id, local_remote_body)

Update email local/remote status

Sets the MTA to treat this domain as either local or remote.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.local_remote_body import LocalRemoteBody
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
    api_instance = openapi_client.EmailsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    domain_id = 'domain_id_example' # str | The id of the domain.
    local_remote_body = openapi_client.LocalRemoteBody() # LocalRemoteBody | 

    try:
        # Update email local/remote status
        api_instance.set_domain_local_remote(org_id, website_id, domain_id, local_remote_body)
    except Exception as e:
        print("Exception when calling EmailsApi->set_domain_local_remote: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **domain_id** | **str**| The id of the domain. | 
 **local_remote_body** | [**LocalRemoteBody**](LocalRemoteBody.md)|  | 

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
**204** | Domain status successfully updated |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_domain_email_auth**
> update_domain_email_auth(org_id, domain_id, email_auth_update)

Update email authentication preferences

Update DKIM setting for the mailboxes on a given domain.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.email_auth_update import EmailAuthUpdate
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
    api_instance = openapi_client.EmailsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    domain_id = 'domain_id_example' # str | The id of the domain.
    email_auth_update = openapi_client.EmailAuthUpdate() # EmailAuthUpdate | Email auth details.

    try:
        # Update email authentication preferences
        api_instance.update_domain_email_auth(org_id, domain_id, email_auth_update)
    except Exception as e:
        print("Exception when calling EmailsApi->update_domain_email_auth: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **domain_id** | **str**| The id of the domain. | 
 **email_auth_update** | [**EmailAuthUpdate**](EmailAuthUpdate.md)| Email auth details. | 

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
**200** | Email auth settings successfully updated |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_website_email**
> update_website_email(org_id, website_id, email_id, update_email)

Update website email

Updates the given email belonging to the given website. The email may have a mailbox or it may be a forwarder, which means it merely serves to forward incoming emails to the specified email addresses. If `hasMailbox` is set to false, the mailbox is deleted if it hadn't existed before, and vice versa. The email must either have a mailbox or forwarders an it must always have a delivery route. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.update_email import UpdateEmail
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
    api_instance = openapi_client.EmailsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    email_id = 'email_id_example' # str | The id of the email.
    update_email = openapi_client.UpdateEmail() # UpdateEmail | Email update details.

    try:
        # Update website email
        api_instance.update_website_email(org_id, website_id, email_id, update_email)
    except Exception as e:
        print("Exception when calling EmailsApi->update_website_email: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **email_id** | **str**| The id of the email. | 
 **update_email** | [**UpdateEmail**](UpdateEmail.md)| Email update details. | 

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
**200** | Email successfully updated |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_website_email_autoresponder**
> update_website_email_autoresponder(org_id, website_id, email_id, autoresponder_id, update_autoresponder)

Update website email autoresponder

Updates the autoresponder belonging to the given website email. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.update_autoresponder import UpdateAutoresponder
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
    api_instance = openapi_client.EmailsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    email_id = 'email_id_example' # str | The id of the email.
    autoresponder_id = 56 # int | The id of the autoresponder.
    update_autoresponder = openapi_client.UpdateAutoresponder() # UpdateAutoresponder | Autoresponder update details.

    try:
        # Update website email autoresponder
        api_instance.update_website_email_autoresponder(org_id, website_id, email_id, autoresponder_id, update_autoresponder)
    except Exception as e:
        print("Exception when calling EmailsApi->update_website_email_autoresponder: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **email_id** | **str**| The id of the email. | 
 **autoresponder_id** | **int**| The id of the autoresponder. | 
 **update_autoresponder** | [**UpdateAutoresponder**](UpdateAutoresponder.md)| Autoresponder update details. | 

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
**200** | Email successfully updated |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **validate_domain_email_auth**
> EmailAuthValidation validate_domain_email_auth(org_id, domain_id)

Validate email authentication DNS records

Validate DKIM and SPF.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.email_auth_validation import EmailAuthValidation
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
    api_instance = openapi_client.EmailsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Validate email authentication DNS records
        api_response = api_instance.validate_domain_email_auth(org_id, domain_id)
        print("The response of EmailsApi->validate_domain_email_auth:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmailsApi->validate_domain_email_auth: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **domain_id** | **str**| The id of the domain. | 

### Return type

[**EmailAuthValidation**](EmailAuthValidation.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Validation response |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

