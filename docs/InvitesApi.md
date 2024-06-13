# openapi_client.InvitesApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**accept_invite**](InvitesApi.md#accept_invite) | **POST** /invites/{invite_id} | Accept invite
[**create_invite**](InvitesApi.md#create_invite) | **POST** /orgs/{org_id}/invites | Create invite
[**validate_invite**](InvitesApi.md#validate_invite) | **POST** /invites/{invite_id}/validate | Validate invite


# **accept_invite**
> accept_invite(invite_id, accept_invite_body=accept_invite_body)

Accept invite

Accepts the invite. There are four cases that need to be handled: No login session is present, user is newly invited and does not yet have a password. The password submitted in the body is set on the new user and the login's member is marked as active within the organization. A session is created and set in the returned cookie. No login session is present but user already exists and has a password. The password submitted in the request body is used to validate the login and the login's member is marked as active within the organization. A session is created and set in the returned cookie. A login session is present for the user to whom the invite belongs. The user is marked active within the organisation to which it was invited. A login session is present for a login to whom the invite does not belong, resulting in an error.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.accept_invite_body import AcceptInviteBody
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
    api_instance = openapi_client.InvitesApi(api_client)
    invite_id = 'invite_id_example' # str | The id of the invite.
    accept_invite_body = openapi_client.AcceptInviteBody() # AcceptInviteBody | Login credentials. (optional)

    try:
        # Accept invite
        api_instance.accept_invite(invite_id, accept_invite_body=accept_invite_body)
    except Exception as e:
        print("Exception when calling InvitesApi->accept_invite: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **invite_id** | **str**| The id of the invite. | 
 **accept_invite_body** | [**AcceptInviteBody**](AcceptInviteBody.md)| Login credentials. | [optional] 

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
**200** | Invite accepted |  * Set-Cookie -  <br>  |
**403** | Session does not belong to invited user |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_invite**
> str create_invite(org_id, new_invite)

Create invite

Issues an invite for the user with the given email. The user may or may not have an account in the realm that the organization is in: If the user is not registered yet, a pending login entry is created for them along with a pending member entry, and the login is \"activated\" once the user accepts the invite. In this case they need to supply a password. If the user is already registered, their existing login is linked to a pending member entry that gets \"activated\" once the user accepts the invite. The sent out invite contains the following URL: http://{control_panel_domain}/invites/{invite_key}?email={user_email} The invite is also returned as a string response for immediate display to the creator of the invite. Where control panel domain is the domain name of the reseller's or the MO's control panel, the invite key is randomly generated, and the user email is the email address to which the invite is sent (and can be used by the API consumer e.g. for display purposes). If the invite is issued for the same organization and email more than once, the invite email is simply sent out again, with a different invite token. The routine will fail if the login already has membership in the organization. Session holder must be at least a `SuperAdmin` in this org or a parent org.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_invite import NewInvite
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
    api_instance = openapi_client.InvitesApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    new_invite = openapi_client.NewInvite() # NewInvite | Invite details.

    try:
        # Create invite
        api_response = api_instance.create_invite(org_id, new_invite)
        print("The response of InvitesApi->create_invite:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InvitesApi->create_invite: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **new_invite** | [**NewInvite**](NewInvite.md)| Invite details. | 

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
**201** | Invite successfully created |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **validate_invite**
> InviteValidation validate_invite(invite_id)

Validate invite

Validates the invite. If successful, it returns the invite details: the organization's id and name, and the to-be-member's role. No session required.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.invite_validation import InviteValidation
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
    api_instance = openapi_client.InvitesApi(api_client)
    invite_id = 'invite_id_example' # str | The id of the invite.

    try:
        # Validate invite
        api_response = api_instance.validate_invite(invite_id)
        print("The response of InvitesApi->validate_invite:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InvitesApi->validate_invite: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **invite_id** | **str**| The id of the invite. | 

### Return type

[**InviteValidation**](InviteValidation.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

