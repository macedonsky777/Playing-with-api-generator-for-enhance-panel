# openapi_client.MembersApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_access_token**](MembersApi.md#create_access_token) | **POST** /orgs/{org_id}/access_tokens | Create organisation access token
[**create_member**](MembersApi.md#create_member) | **POST** /orgs/{org_id}/members | Create organization member
[**delete_access_token**](MembersApi.md#delete_access_token) | **DELETE** /orgs/{org_id}/access_tokens/{token_id} | Delete access token member
[**delete_member**](MembersApi.md#delete_member) | **DELETE** /orgs/{org_id}/members/{member_id} | Delete organization member
[**delete_owner**](MembersApi.md#delete_owner) | **DELETE** /orgs/{org_id}/owner | Delete organization owner
[**get_access_tokens**](MembersApi.md#get_access_tokens) | **GET** /orgs/{org_id}/access_tokens | Get access token members
[**get_member**](MembersApi.md#get_member) | **GET** /orgs/{org_id}/members/{member_id} | Get organization member
[**get_members**](MembersApi.md#get_members) | **GET** /orgs/{org_id}/members | Get organization members
[**get_org_member_login**](MembersApi.md#get_org_member_login) | **GET** /orgs/{org_id}/members/{member_id}/sso | Get a One-Time-Password link for the member
[**update_member**](MembersApi.md#update_member) | **PUT** /orgs/{org_id}/members/{member_id} | Overwrite organization member settings
[**update_owner**](MembersApi.md#update_owner) | **PUT** /orgs/{org_id}/owner | Update organization owner


# **create_access_token**
> NewAccessTokenResponse create_access_token(org_id, new_access_token)

Create organisation access token

Create an access token with rights within an organisation.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_access_token import NewAccessToken
from openapi_client.models.new_access_token_response import NewAccessTokenResponse
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
    api_instance = openapi_client.MembersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    new_access_token = openapi_client.NewAccessToken() # NewAccessToken | Access token details

    try:
        # Create organisation access token
        api_response = api_instance.create_access_token(org_id, new_access_token)
        print("The response of MembersApi->create_access_token:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MembersApi->create_access_token: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **new_access_token** | [**NewAccessToken**](NewAccessToken.md)| Access token details | 

### Return type

[**NewAccessTokenResponse**](NewAccessTokenResponse.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Token successfully created |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |
**409** | Already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_member**
> NewResourceUuid create_member(org_id, new_member)

Create organization member

A login for the member needs to exist before establishing membership. On success, the member id is returned. This operation can only be done by a logged in superadmin or owner of the organization or its parent organization(s).

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_member import NewMember
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
    api_instance = openapi_client.MembersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    new_member = openapi_client.NewMember() # NewMember | New member details

    try:
        # Create organization member
        api_response = api_instance.create_member(org_id, new_member)
        print("The response of MembersApi->create_member:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MembersApi->create_member: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **new_member** | [**NewMember**](NewMember.md)| New member details | 

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
**201** | Member successfully created |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |
**409** | Already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_access_token**
> delete_access_token(org_id, token_id)

Delete access token member

Delete an access token

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
    api_instance = openapi_client.MembersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    token_id = 'token_id_example' # str | The id of an org access token.

    try:
        # Delete access token member
        api_instance.delete_access_token(org_id, token_id)
    except Exception as e:
        print("Exception when calling MembersApi->delete_access_token: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **token_id** | **str**| The id of an org access token. | 

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
**204** | Deleted |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_member**
> delete_member(org_id, member_id)

Delete organization member

This operation can only be done by a logged in superadmin or owner of the organization or its parent organization(s).

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
    api_instance = openapi_client.MembersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    member_id = 'member_id_example' # str | The id of the member.

    try:
        # Delete organization member
        api_instance.delete_member(org_id, member_id)
    except Exception as e:
        print("Exception when calling MembersApi->delete_member: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **member_id** | **str**| The id of the member. | 

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
**204** | Member successfully deleted |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_owner**
> delete_owner(org_id)

Delete organization owner

This operation can only be done by a logged in superadmin of the organization's parent organization (TODO it's unclear as of this writing whether organization owners may delete themselves). The previous owner is demoted to the \"SupperAdmin\" role.

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
    api_instance = openapi_client.MembersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.

    try:
        # Delete organization owner
        api_instance.delete_owner(org_id)
    except Exception as e:
        print("Exception when calling MembersApi->delete_owner: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 

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
**204** | Owner successfully deleted |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_access_tokens**
> List[OrgAccessToken] get_access_tokens(org_id)

Get access token members

Returns all access tokens belonging to the organisation

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.org_access_token import OrgAccessToken
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
    api_instance = openapi_client.MembersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.

    try:
        # Get access token members
        api_response = api_instance.get_access_tokens(org_id)
        print("The response of MembersApi->get_access_tokens:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MembersApi->get_access_tokens: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 

### Return type

[**List[OrgAccessToken]**](OrgAccessToken.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Access tokens successfully queried |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_member**
> Member get_member(org_id, member_id)

Get organization member

Returns details about this organization member. This operation can only be done by the member itself, a logged in superadmin or owner of the organization or its parent organization(s).

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.member import Member
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
    api_instance = openapi_client.MembersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    member_id = 'member_id_example' # str | The id of the member.

    try:
        # Get organization member
        api_response = api_instance.get_member(org_id, member_id)
        print("The response of MembersApi->get_member:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MembersApi->get_member: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **member_id** | **str**| The id of the member. | 

### Return type

[**Member**](Member.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Member successfully queried |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_members**
> MembersListing get_members(org_id, offset=offset, limit=limit, sort_by=sort_by, sort_order=sort_order, search=search, role=role, site_access=site_access)

Get organization members

Returns all (both pending and full) members of the organization. Session holder must be at least a `SuperAdmin` in this org or a parent org.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.members_listing import MembersListing
from openapi_client.models.role import Role
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
    api_instance = openapi_client.MembersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    offset = 56 # int | The offset from which to return items. (optional)
    limit = 56 # int | The maximum number of items to return. (optional)
    sort_by = 'sort_by_example' # str | The field by which to sort. (optional)
    sort_order = 'sort_order_example' # str | The direction in which to sort. Possible values are 'asc' and 'desc', defaulting to 'asc'. (optional)
    search = 'search_example' # str | Limit the result set to the resources whose names, partially and case insensitively, match the specified search term. E.g. for websites, this is their domain or tag, for databases the database name, for emails the email address or mailbox name, etc. A website will also be returned if the search term exactly matches the website's uuid. (optional)
    role = openapi_client.Role() # Role | Return only members with this role. (optional)
    site_access = 'site_access_example' # str | Return only collaborator members that have access to this website. Note that super admins and owners are not returned because they implicitly have access. (optional)

    try:
        # Get organization members
        api_response = api_instance.get_members(org_id, offset=offset, limit=limit, sort_by=sort_by, sort_order=sort_order, search=search, role=role, site_access=site_access)
        print("The response of MembersApi->get_members:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MembersApi->get_members: %s\n" % e)
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
 **role** | [**Role**](.md)| Return only members with this role. | [optional] 
 **site_access** | **str**| Return only collaborator members that have access to this website. Note that super admins and owners are not returned because they implicitly have access. | [optional] 

### Return type

[**MembersListing**](MembersListing.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Members successfully queried |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_org_member_login**
> str get_org_member_login(org_id, member_id)

Get a One-Time-Password link for the member

Returns a short lived one time password link for direct log-ins via the users realm. Session holder must be an `Owner`, `SuperAdmin` or `Sysadmin` in the org or the MO.

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
    api_instance = openapi_client.MembersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    member_id = 'member_id_example' # str | The id of the member.

    try:
        # Get a One-Time-Password link for the member
        api_response = api_instance.get_org_member_login(org_id, member_id)
        print("The response of MembersApi->get_org_member_login:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MembersApi->get_org_member_login: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **member_id** | **str**| The id of the member. | 

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
**201** | OTP login link successfully created |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_member**
> update_member(org_id, member_id, update_member)

Overwrite organization member settings

Updates member information, such as their roles, site access permissions, and notification settings. This operation can only be done by the logged in superadmin or owner of the organization or its parent organization(s). This operation overwrites existing settings, so all existing values that are meant to be kept should be included in the response body.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.update_member import UpdateMember
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
    api_instance = openapi_client.MembersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    member_id = 'member_id_example' # str | The id of the member.
    update_member = openapi_client.UpdateMember() # UpdateMember | Member settings

    try:
        # Overwrite organization member settings
        api_instance.update_member(org_id, member_id, update_member)
    except Exception as e:
        print("Exception when calling MembersApi->update_member: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **member_id** | **str**| The id of the member. | 
 **update_member** | [**UpdateMember**](UpdateMember.md)| Member settings | 

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
**200** | Member settings successfully updated |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_owner**
> update_owner(org_id, org_owner_update)

Update organization owner

The new owner must already be a member in the organization before establishing ownership. This operation can only be done by a logged in superadmin of the organization's parent organization, or the owner of the organization. In both cases, the previous owner (if they existed) is demoted to SuperAdmin after this operation.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.org_owner_update import OrgOwnerUpdate
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
    api_instance = openapi_client.MembersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    org_owner_update = openapi_client.OrgOwnerUpdate() # OrgOwnerUpdate | Membership id of the to-be owner

    try:
        # Update organization owner
        api_instance.update_owner(org_id, org_owner_update)
    except Exception as e:
        print("Exception when calling MembersApi->update_owner: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **org_owner_update** | [**OrgOwnerUpdate**](OrgOwnerUpdate.md)| Membership id of the to-be owner | 

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
**200** | Owner successfully updated |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

