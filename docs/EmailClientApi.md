# openapi_client.EmailClientApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_email_autoresponder**](EmailClientApi.md#create_email_autoresponder) | **POST** /email-client/autoresponders | Create new email autoresponder
[**delete_email_autoresponder**](EmailClientApi.md#delete_email_autoresponder) | **DELETE** /email-client/autoresponders/{autoresponder_id} | Delete email autoresponder
[**get_email_autoresponders**](EmailClientApi.md#get_email_autoresponders) | **GET** /email-client/autoresponders | Get email account autoresponders
[**get_email_forwarders**](EmailClientApi.md#get_email_forwarders) | **GET** /email-client/forwarders | Returns email account&#39;s forwarders
[**get_email_public_ip**](EmailClientApi.md#get_email_public_ip) | **GET** /email-client/public-ip | Returns public Ip Address of the email server
[**update_email_autoresponder**](EmailClientApi.md#update_email_autoresponder) | **PUT** /email-client/autoresponders/{autoresponder_id} | Update email autoresponder
[**update_email_forwarders**](EmailClientApi.md#update_email_forwarders) | **PUT** /email-client/forwarders | Updates email account&#39;s forwarders
[**update_email_password**](EmailClientApi.md#update_email_password) | **PUT** /email-client/password | Updates email account&#39;s password


# **create_email_autoresponder**
> NewResourceId create_email_autoresponder(authorization, address, password, new_autoresponder)

Create new email autoresponder

Creates a new autoresponder for the given email. Client must send Authorization token, email address and its current password for authentication

### Example


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


# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.EmailClientApi(api_client)
    authorization = 'authorization_example' # str | 
    address = 'address_example' # str | 
    password = 'password_example' # str | 
    new_autoresponder = openapi_client.NewAutoresponder() # NewAutoresponder | Autoresponder details.

    try:
        # Create new email autoresponder
        api_response = api_instance.create_email_autoresponder(authorization, address, password, new_autoresponder)
        print("The response of EmailClientApi->create_email_autoresponder:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmailClientApi->create_email_autoresponder: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **str**|  | 
 **address** | **str**|  | 
 **password** | **str**|  | 
 **new_autoresponder** | [**NewAutoresponder**](NewAutoresponder.md)| Autoresponder details. | 

### Return type

[**NewResourceId**](NewResourceId.md)

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
**401** | Unauthorized |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |
**409** | Already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_email_autoresponder**
> delete_email_autoresponder(authorization, address, password, autoresponder_id)

Delete email autoresponder

Deletes the autoresponder belonging to the given email account. Client must send Authorization token, email address and its current   password for authentication

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
    api_instance = openapi_client.EmailClientApi(api_client)
    authorization = 'authorization_example' # str | 
    address = 'address_example' # str | 
    password = 'password_example' # str | 
    autoresponder_id = 56 # int | The id of the autoresponder.

    try:
        # Delete email autoresponder
        api_instance.delete_email_autoresponder(authorization, address, password, autoresponder_id)
    except Exception as e:
        print("Exception when calling EmailClientApi->delete_email_autoresponder: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **str**|  | 
 **address** | **str**|  | 
 **password** | **str**|  | 
 **autoresponder_id** | **int**| The id of the autoresponder. | 

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
**204** | Autoresponder successfully deleted |  -  |
**401** | Unauthorized |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_email_autoresponders**
> AutorespondersFullListing get_email_autoresponders(authorization, address, password)

Get email account autoresponders

Returns autoresponders configured for the given email. Client must send Authorization token, email address and its current password for authentication

### Example


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


# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.EmailClientApi(api_client)
    authorization = 'authorization_example' # str | 
    address = 'address_example' # str | 
    password = 'password_example' # str | 

    try:
        # Get email account autoresponders
        api_response = api_instance.get_email_autoresponders(authorization, address, password)
        print("The response of EmailClientApi->get_email_autoresponders:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmailClientApi->get_email_autoresponders: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **str**|  | 
 **address** | **str**|  | 
 **password** | **str**|  | 

### Return type

[**AutorespondersFullListing**](AutorespondersFullListing.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Autoresponders successfully queried |  -  |
**401** | Unauthorized |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_email_forwarders**
> ForwardersFullListing get_email_forwarders(authorization, address, password)

Returns email account's forwarders

Returns forwarders list for the given email account. Client must send Authorization token, email address and its current password for authentication

### Example


```python
import openapi_client
from openapi_client.models.forwarders_full_listing import ForwardersFullListing
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
    api_instance = openapi_client.EmailClientApi(api_client)
    authorization = 'authorization_example' # str | 
    address = 'address_example' # str | 
    password = 'password_example' # str | 

    try:
        # Returns email account's forwarders
        api_response = api_instance.get_email_forwarders(authorization, address, password)
        print("The response of EmailClientApi->get_email_forwarders:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmailClientApi->get_email_forwarders: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **str**|  | 
 **address** | **str**|  | 
 **password** | **str**|  | 

### Return type

[**ForwardersFullListing**](ForwardersFullListing.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Forwarders successfully queried |  -  |
**400** | Invalid input |  -  |
**401** | Unauthorized |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_email_public_ip**
> EmailPublicIp get_email_public_ip(authorization, address, password)

Returns public Ip Address of the email server

### Example


```python
import openapi_client
from openapi_client.models.email_public_ip import EmailPublicIp
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
    api_instance = openapi_client.EmailClientApi(api_client)
    authorization = 'authorization_example' # str | 
    address = 'address_example' # str | 
    password = 'password_example' # str | 

    try:
        # Returns public Ip Address of the email server
        api_response = api_instance.get_email_public_ip(authorization, address, password)
        print("The response of EmailClientApi->get_email_public_ip:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmailClientApi->get_email_public_ip: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **str**|  | 
 **address** | **str**|  | 
 **password** | **str**|  | 

### Return type

[**EmailPublicIp**](EmailPublicIp.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Public IP address for email server |  -  |
**400** | Invalid input |  -  |
**401** | Unauthorized |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_email_autoresponder**
> update_email_autoresponder(authorization, address, password, autoresponder_id, update_autoresponder)

Update email autoresponder

Updates the autoresponder belonging to the given email account. Client must send Authorization token, email address and its current password for authentication

### Example


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


# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.EmailClientApi(api_client)
    authorization = 'authorization_example' # str | 
    address = 'address_example' # str | 
    password = 'password_example' # str | 
    autoresponder_id = 56 # int | The id of the autoresponder.
    update_autoresponder = openapi_client.UpdateAutoresponder() # UpdateAutoresponder | Autoresponder update details.

    try:
        # Update email autoresponder
        api_instance.update_email_autoresponder(authorization, address, password, autoresponder_id, update_autoresponder)
    except Exception as e:
        print("Exception when calling EmailClientApi->update_email_autoresponder: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **str**|  | 
 **address** | **str**|  | 
 **password** | **str**|  | 
 **autoresponder_id** | **int**| The id of the autoresponder. | 
 **update_autoresponder** | [**UpdateAutoresponder**](UpdateAutoresponder.md)| Autoresponder update details. | 

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
**401** | Unauthorized |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_email_forwarders**
> update_email_forwarders(authorization, address, password, email_forwarders_update)

Updates email account's forwarders

Accepts forwarders list in body. Client must send Authorization token, email address and its current password for authentication

### Example


```python
import openapi_client
from openapi_client.models.email_forwarders_update import EmailForwardersUpdate
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
    api_instance = openapi_client.EmailClientApi(api_client)
    authorization = 'authorization_example' # str | 
    address = 'address_example' # str | 
    password = 'password_example' # str | 
    email_forwarders_update = openapi_client.EmailForwardersUpdate() # EmailForwardersUpdate | 

    try:
        # Updates email account's forwarders
        api_instance.update_email_forwarders(authorization, address, password, email_forwarders_update)
    except Exception as e:
        print("Exception when calling EmailClientApi->update_email_forwarders: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **str**|  | 
 **address** | **str**|  | 
 **password** | **str**|  | 
 **email_forwarders_update** | [**EmailForwardersUpdate**](EmailForwardersUpdate.md)|  | 

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
**200** | Successful |  -  |
**400** | Invalid input |  -  |
**401** | Unauthorized |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_email_password**
> update_email_password(authorization, address, password, email_password_update)

Updates email account's password

Accepts a new password in body. Client must send Authorization token, email address and its current password for authentication

### Example


```python
import openapi_client
from openapi_client.models.email_password_update import EmailPasswordUpdate
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
    api_instance = openapi_client.EmailClientApi(api_client)
    authorization = 'authorization_example' # str | 
    address = 'address_example' # str | 
    password = 'password_example' # str | 
    email_password_update = openapi_client.EmailPasswordUpdate() # EmailPasswordUpdate | 

    try:
        # Updates email account's password
        api_instance.update_email_password(authorization, address, password, email_password_update)
    except Exception as e:
        print("Exception when calling EmailClientApi->update_email_password: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **str**|  | 
 **address** | **str**|  | 
 **password** | **str**|  | 
 **email_password_update** | [**EmailPasswordUpdate**](EmailPasswordUpdate.md)|  | 

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
**200** | Successful |  -  |
**400** | Invalid input |  -  |
**401** | Unauthorized |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

