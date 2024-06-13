# openapi_client.LoginsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_login**](LoginsApi.md#create_login) | **POST** /logins | Create a new login
[**create_otp_session**](LoginsApi.md#create_otp_session) | **GET** /login/sessions/sso | Create a new session for login with a one-time-password
[**create_session**](LoginsApi.md#create_session) | **POST** /login/sessions | Create a new session for login
[**delete_current_session**](LoginsApi.md#delete_current_session) | **DELETE** /login/sessions/current | Delete current session
[**delete_login_avatar**](LoginsApi.md#delete_login_avatar) | **DELETE** /login/avatar | Remove login avatar
[**delete_session**](LoginsApi.md#delete_session) | **DELETE** /login/sessions/{session_id} | Delete current session
[**delete_sessions**](LoginsApi.md#delete_sessions) | **DELETE** /login/sessions | Delete sessions
[**finish_password_recovery**](LoginsApi.md#finish_password_recovery) | **POST** /login/password-recovery | Finish a password recovery
[**get_customer_logins**](LoginsApi.md#get_customer_logins) | **GET** /v2/orgs/{org_id}/customers/logins | List customer logins for org
[**get_login**](LoginsApi.md#get_login) | **GET** /login | Get login info
[**get_login_memberships**](LoginsApi.md#get_login_memberships) | **GET** /login/memberships | Get login memberships
[**get_logins**](LoginsApi.md#get_logins) | **GET** /logins | Query all logins
[**get_org_logins**](LoginsApi.md#get_org_logins) | **GET** /orgs/{org_id}/logins | Query logins belonging to organization
[**get_sessions**](LoginsApi.md#get_sessions) | **GET** /login/sessions | Get all login sessions
[**resend_pin**](LoginsApi.md#resend_pin) | **POST** /login/2fa/resend-pin | Resends 2FA sign-in code.
[**set_customer_login_password**](LoginsApi.md#set_customer_login_password) | **PUT** /v2/logins/{login_id}/password | Set password for login
[**set_login_avatar**](LoginsApi.md#set_login_avatar) | **PUT** /login/avatar | Set login avatar
[**start_password_recovery**](LoginsApi.md#start_password_recovery) | **PUT** /login/password-recovery | Start a new password recovery for login
[**update_login_info**](LoginsApi.md#update_login_info) | **PATCH** /login | Update login info
[**validate_password_recovery**](LoginsApi.md#validate_password_recovery) | **POST** /login/password-recovery/validate | Validate a password recovery secret
[**verify2_fa**](LoginsApi.md#verify2_fa) | **POST** /login/2fa | Verifies 2FA sign-in code.


# **create_login**
> NewResourceUuid create_login(org_id, login_info)

Create a new login

Creates a login in the realm. The login will be created in the same realm that the organization is in. Session holder must have admin or support privileges in the given organization or any parent thereof.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.login_info import LoginInfo
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
    api_instance = openapi_client.LoginsApi(api_client)
    org_id = 'org_id_example' # str | The mandatory organization id to denote in which realm to create the login in. The login will be created in the same realm that the organization is in.
    login_info = openapi_client.LoginInfo() # LoginInfo | 

    try:
        # Create a new login
        api_response = api_instance.create_login(org_id, login_info)
        print("The response of LoginsApi->create_login:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LoginsApi->create_login: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The mandatory organization id to denote in which realm to create the login in. The login will be created in the same realm that the organization is in. | 
 **login_info** | [**LoginInfo**](LoginInfo.md)|  | 

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
**409** | Already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_otp_session**
> LoginMemberships create_otp_session(otp)

Create a new session for login with a one-time-password

Creates a new session for the login in a specific login realm, using a short lived one time password. This creates a session as well, with the difference that realmId is required and any 2FA will be bypassed.

### Example


```python
import openapi_client
from openapi_client.models.login_memberships import LoginMemberships
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
    api_instance = openapi_client.LoginsApi(api_client)
    otp = 'otp_example' # str | Contains a short lived otp for direct login bypassing any 2FA.

    try:
        # Create a new session for login with a one-time-password
        api_response = api_instance.create_otp_session(otp)
        print("The response of LoginsApi->create_otp_session:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LoginsApi->create_otp_session: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **otp** | **str**| Contains a short lived otp for direct login bypassing any 2FA. | 

### Return type

[**LoginMemberships**](LoginMemberships.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  * Set-Cookie -  <br>  |
**400** | Invalid input |  -  |
**401** | Invalid credentials |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_session**
> LoginMemberships create_session(login_creds, realm_id=realm_id)

Create a new session for login

Creates a new session for the login in a specific login realm. By default, the realm in which to look up a given login is dictated by the domain on which the request is made.  If it matches a mapped to a ControlPanel website belonging to an MO or a reseller then that MO or reseller is used as the relam from which to select the login.  If the login exists directly as a member of the chosen realm then that login will be selected in preference to any which exists within the realm itself. The realm derived from the control panel domain can be overridden with the realmId parameter to specify a particular reseller or the MO. The authentication result is a JWT session token and a list detailing the organizations in which login is a member. In case of 2FA, the authentication result is a JWT session token with empty body and 201 http status code.

### Example


```python
import openapi_client
from openapi_client.models.login_creds import LoginCreds
from openapi_client.models.login_memberships import LoginMemberships
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
    api_instance = openapi_client.LoginsApi(api_client)
    login_creds = openapi_client.LoginCreds() # LoginCreds | Login credentials.
    realm_id = 'realm_id_example' # str | If set with the given realm's id (the parent id of an organization), then the login is authenticated in this realm. See the endpoint description for more info. (optional)

    try:
        # Create a new session for login
        api_response = api_instance.create_session(login_creds, realm_id=realm_id)
        print("The response of LoginsApi->create_session:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LoginsApi->create_session: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **login_creds** | [**LoginCreds**](LoginCreds.md)| Login credentials. | 
 **realm_id** | **str**| If set with the given realm&#39;s id (the parent id of an organization), then the login is authenticated in this realm. See the endpoint description for more info. | [optional] 

### Return type

[**LoginMemberships**](LoginMemberships.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  * Set-Cookie -  <br>  |
**201** | Verification pin was created |  * Set-Cookie -  <br>  |
**400** | Invalid input |  -  |
**401** | Invalid credentials |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_current_session**
> delete_current_session()

Delete current session

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
    api_instance = openapi_client.LoginsApi(api_client)

    try:
        # Delete current session
        api_instance.delete_current_session()
    except Exception as e:
        print("Exception when calling LoginsApi->delete_current_session: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

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
**200** | Successful |  * Set-Cookie -  <br>  |
**401** | Invalid session |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_login_avatar**
> delete_login_avatar()

Remove login avatar

Deletes the user's avatar. The user is implicitly assumed to be the session holder, so no login id is supplied.

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
    api_instance = openapi_client.LoginsApi(api_client)

    try:
        # Remove login avatar
        api_instance.delete_login_avatar()
    except Exception as e:
        print("Exception when calling LoginsApi->delete_login_avatar: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

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
**204** | Successful |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_session**
> delete_session(session_id)

Delete current session

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
    api_instance = openapi_client.LoginsApi(api_client)
    session_id = 'session_id_example' # str | The id of the login session.

    try:
        # Delete current session
        api_instance.delete_session(session_id)
    except Exception as e:
        print("Exception when calling LoginsApi->delete_session: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **session_id** | **str**| The id of the login session. | 

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
**200** | Successful |  * Set-Cookie -  <br>  |
**401** | Invalid session |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_sessions**
> delete_sessions()

Delete sessions

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
    api_instance = openapi_client.LoginsApi(api_client)

    try:
        # Delete sessions
        api_instance.delete_sessions()
    except Exception as e:
        print("Exception when calling LoginsApi->delete_sessions: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

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
**200** | Successful |  * Set-Cookie -  <br>  |
**401** | Invalid session |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **finish_password_recovery**
> finish_password_recovery(secret, new_password)

Finish a password recovery

Finishes the password recovery for the recovery key. This operation only succeeds if the key hasn't expired. If it has, the user must initiate a new password recovery.

### Example


```python
import openapi_client
from openapi_client.models.new_password import NewPassword
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
    api_instance = openapi_client.LoginsApi(api_client)
    secret = 'secret_example' # str | The secret key for the password recovery.
    new_password = openapi_client.NewPassword() # NewPassword | Login's new password.

    try:
        # Finish a password recovery
        api_instance.finish_password_recovery(secret, new_password)
    except Exception as e:
        print("Exception when calling LoginsApi->finish_password_recovery: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **secret** | **str**| The secret key for the password recovery. | 
 **new_password** | [**NewPassword**](NewPassword.md)| Login&#39;s new password. | 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_customer_logins**
> LoginsListing get_customer_logins(org_id, offset=offset, limit=limit, sort_order=sort_order, sort_by=sort_by)

List customer logins for org

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.logins_listing import LoginsListing
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
    api_instance = openapi_client.LoginsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    offset = 56 # int | The offset from which to return items. (optional)
    limit = 56 # int | The maximum number of items to return. (optional)
    sort_order = 'sort_order_example' # str | The direction in which to sort. Possible values are 'asc' and 'desc', defaulting to 'asc'. (optional)
    sort_by = 'sort_by_example' # str | The field by which to sort. (optional)

    try:
        # List customer logins for org
        api_response = api_instance.get_customer_logins(org_id, offset=offset, limit=limit, sort_order=sort_order, sort_by=sort_by)
        print("The response of LoginsApi->get_customer_logins:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LoginsApi->get_customer_logins: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **offset** | **int**| The offset from which to return items. | [optional] 
 **limit** | **int**| The maximum number of items to return. | [optional] 
 **sort_order** | **str**| The direction in which to sort. Possible values are &#39;asc&#39; and &#39;desc&#39;, defaulting to &#39;asc&#39;. | [optional] 
 **sort_by** | **str**| The field by which to sort. | [optional] 

### Return type

[**LoginsListing**](LoginsListing.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Logins successfully queried |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_login**
> Login get_login()

Get login info

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.login import Login
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
    api_instance = openapi_client.LoginsApi(api_client)

    try:
        # Get login info
        api_response = api_instance.get_login()
        print("The response of LoginsApi->get_login:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LoginsApi->get_login: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**Login**](Login.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_login_memberships**
> LoginMemberships get_login_memberships()

Get login memberships

Returns a list of info about all organization's the login is a member of. The return value is the same as that of successful session creation.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.login_memberships import LoginMemberships
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
    api_instance = openapi_client.LoginsApi(api_client)

    try:
        # Get login memberships
        api_response = api_instance.get_login_memberships()
        print("The response of LoginsApi->get_login_memberships:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LoginsApi->get_login_memberships: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**LoginMemberships**](LoginMemberships.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Memberships successfully queried |  -  |
**401** | Invalid session |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_logins**
> LoginsListing get_logins(realm_id=realm_id, offset=offset, limit=limit, sort_order=sort_order, sort_by=sort_by)

Query all logins

Returns all logins registered in the control panel. Session holder must be an `Owner`, `SuperAdmin`, or `Sysadmin` in the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.logins_listing import LoginsListing
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
    api_instance = openapi_client.LoginsApi(api_client)
    realm_id = 'realm_id_example' # str | The id of the realm to query. Realm ids map to org ids. (optional)
    offset = 56 # int | The offset from which to return items. (optional)
    limit = 56 # int | The maximum number of items to return. (optional)
    sort_order = 'sort_order_example' # str | The direction in which to sort. Possible values are 'asc' and 'desc', defaulting to 'asc'. (optional)
    sort_by = 'sort_by_example' # str | The field by which to sort. (optional)

    try:
        # Query all logins
        api_response = api_instance.get_logins(realm_id=realm_id, offset=offset, limit=limit, sort_order=sort_order, sort_by=sort_by)
        print("The response of LoginsApi->get_logins:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LoginsApi->get_logins: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **realm_id** | **str**| The id of the realm to query. Realm ids map to org ids. | [optional] 
 **offset** | **int**| The offset from which to return items. | [optional] 
 **limit** | **int**| The maximum number of items to return. | [optional] 
 **sort_order** | **str**| The direction in which to sort. Possible values are &#39;asc&#39; and &#39;desc&#39;, defaulting to &#39;asc&#39;. | [optional] 
 **sort_by** | **str**| The field by which to sort. | [optional] 

### Return type

[**LoginsListing**](LoginsListing.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Logins successfully queried |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_org_logins**
> LoginsListing get_org_logins(org_id, offset=offset, limit=limit, sort_order=sort_order, sort_by=sort_by)

Query logins belonging to organization

Returns all logins registered in given organization. Session holder must be an `Owner`, `SuperAdmin` or `Sysadmin` in the org or the MO.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.logins_listing import LoginsListing
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
    api_instance = openapi_client.LoginsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    offset = 56 # int | The offset from which to return items. (optional)
    limit = 56 # int | The maximum number of items to return. (optional)
    sort_order = 'sort_order_example' # str | The direction in which to sort. Possible values are 'asc' and 'desc', defaulting to 'asc'. (optional)
    sort_by = 'sort_by_example' # str | The field by which to sort. (optional)

    try:
        # Query logins belonging to organization
        api_response = api_instance.get_org_logins(org_id, offset=offset, limit=limit, sort_order=sort_order, sort_by=sort_by)
        print("The response of LoginsApi->get_org_logins:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LoginsApi->get_org_logins: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **offset** | **int**| The offset from which to return items. | [optional] 
 **limit** | **int**| The maximum number of items to return. | [optional] 
 **sort_order** | **str**| The direction in which to sort. Possible values are &#39;asc&#39; and &#39;desc&#39;, defaulting to &#39;asc&#39;. | [optional] 
 **sort_by** | **str**| The field by which to sort. | [optional] 

### Return type

[**LoginsListing**](LoginsListing.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Logins successfully queried |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_sessions**
> SessionsFullListing get_sessions()

Get all login sessions

### Example


```python
import openapi_client
from openapi_client.models.sessions_full_listing import SessionsFullListing
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
    api_instance = openapi_client.LoginsApi(api_client)

    try:
        # Get all login sessions
        api_response = api_instance.get_sessions()
        print("The response of LoginsApi->get_sessions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LoginsApi->get_sessions: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**SessionsFullListing**](SessionsFullListing.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid credentials |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **resend_pin**
> resend_pin(resend_pin)

Resends 2FA sign-in code.

On success, standard session with a new pin returned, otherwise 401 Unauthorized is returned with an empty cookie and the session is removed. Note that 2FA can only be used with the session cookie.

### Example

* Api Key Authentication (sessionCookie):

```python
import openapi_client
from openapi_client.models.resend_pin import ResendPin
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

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.LoginsApi(api_client)
    resend_pin = openapi_client.ResendPin() # ResendPin | Verification details.

    try:
        # Resends 2FA sign-in code.
        api_instance.resend_pin(resend_pin)
    except Exception as e:
        print("Exception when calling LoginsApi->resend_pin: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **resend_pin** | [**ResendPin**](ResendPin.md)| Verification details. | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  * Set-Cookie -  <br>  |
**400** | Invalid input |  -  |
**401** | Invalid credentials |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_customer_login_password**
> set_customer_login_password(login_id, new_password)

Set password for login

This operation allows admins to reset the password for a login.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_password import NewPassword
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
    api_instance = openapi_client.LoginsApi(api_client)
    login_id = 'login_id_example' # str | The id of a login.
    new_password = openapi_client.NewPassword() # NewPassword | The new unhashed password to set for the login

    try:
        # Set password for login
        api_instance.set_customer_login_password(login_id, new_password)
    except Exception as e:
        print("Exception when calling LoginsApi->set_customer_login_password: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **login_id** | **str**| The id of a login. | 
 **new_password** | [**NewPassword**](NewPassword.md)| The new unhashed password to set for the login | 

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
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_login_avatar**
> set_login_avatar(avatar=avatar)

Set login avatar

Sets the user's avatar, overwriting any previous one if one exists. The max allowed size is 200 KiB. The image format may be jpeg, png, and ico. The user is implicitly assumed to be the session holder, so no login id is supplied.

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
    api_instance = openapi_client.LoginsApi(api_client)
    avatar = None # bytearray |  (optional)

    try:
        # Set login avatar
        api_instance.set_login_avatar(avatar=avatar)
    except Exception as e:
        print("Exception when calling LoginsApi->set_login_avatar: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **avatar** | **bytearray**|  | [optional] 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **start_password_recovery**
> start_password_recovery(email_address, realm_id=realm_id)

Start a new password recovery for login

Initiates a new password recovery for the given email address, or fails silently (returning a `200 Ok`) if no login corresponded to the email. Note that only logins who are registered may initiate a password recovery. Users who were invited by an org member and haven't finished their signup may not start a recovery.

### Example


```python
import openapi_client
from openapi_client.models.email_address import EmailAddress
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
    api_instance = openapi_client.LoginsApi(api_client)
    email_address = openapi_client.EmailAddress() # EmailAddress | Login's email address.
    realm_id = 'realm_id_example' # str | If set, the login is looked up in the specified realm. If unset then the chosen realm will be based on the control panel hostname. (optional)

    try:
        # Start a new password recovery for login
        api_instance.start_password_recovery(email_address, realm_id=realm_id)
    except Exception as e:
        print("Exception when calling LoginsApi->start_password_recovery: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email_address** | [**EmailAddress**](EmailAddress.md)| Login&#39;s email address. | 
 **realm_id** | **str**| If set, the login is looked up in the specified realm. If unset then the chosen realm will be based on the control panel hostname. | [optional] 

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
**200** | Recovery maybe started |  -  |
**400** | Invalid input |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_login_info**
> UpdateLoginResult update_login_info(update_login)

Update login info

Updates some or all login information and credentials. Only the currently authenticated login may do this (thus there is no explicit login id in the input). If the email or password are to be updated, the current password must be provided. In order to disable MFA, a user has to validate the PIN code required by the enabled method. If users want to switch to a different MFA method, they need to disable MFA and enable the desired MFA method.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.update_login import UpdateLogin
from openapi_client.models.update_login_result import UpdateLoginResult
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
    api_instance = openapi_client.LoginsApi(api_client)
    update_login = openapi_client.UpdateLogin() # UpdateLogin | 

    try:
        # Update login info
        api_response = api_instance.update_login_info(update_login)
        print("The response of LoginsApi->update_login_info:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LoginsApi->update_login_info: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **update_login** | [**UpdateLogin**](UpdateLogin.md)|  | 

### Return type

[**UpdateLoginResult**](UpdateLoginResult.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Current password missing |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **validate_password_recovery**
> ValidatedPasswordRecovery validate_password_recovery(secret)

Validate a password recovery secret

Returns the obfuscated email address belonging to the user initiating the password recovery if the secret is correct and hasn't expired yet.

### Example


```python
import openapi_client
from openapi_client.models.validated_password_recovery import ValidatedPasswordRecovery
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
    api_instance = openapi_client.LoginsApi(api_client)
    secret = 'secret_example' # str | The secret key for the password recovery.

    try:
        # Validate a password recovery secret
        api_response = api_instance.validate_password_recovery(secret)
        print("The response of LoginsApi->validate_password_recovery:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LoginsApi->validate_password_recovery: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **secret** | **str**| The secret key for the password recovery. | 

### Return type

[**ValidatedPasswordRecovery**](ValidatedPasswordRecovery.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**400** | Invalid input |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **verify2_fa**
> verify2_fa(login2_fa)

Verifies 2FA sign-in code.

On success, standard session with cookie is returned, otherwise 401 Unauthorized is returned with an empty cookie and the session is removed. Note that 2FA can only be used with the session cookie.

### Example

* Api Key Authentication (sessionCookie):

```python
import openapi_client
from openapi_client.models.login2_fa import Login2FA
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

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.LoginsApi(api_client)
    login2_fa = openapi_client.Login2FA() # Login2FA | Verification details.

    try:
        # Verifies 2FA sign-in code.
        api_instance.verify2_fa(login2_fa)
    except Exception as e:
        print("Exception when calling LoginsApi->verify2_fa: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **login2_fa** | [**Login2FA**](Login2FA.md)| Verification details. | 

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  * Set-Cookie -  <br>  |
**400** | Invalid input |  -  |
**401** | Invalid credentials |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

