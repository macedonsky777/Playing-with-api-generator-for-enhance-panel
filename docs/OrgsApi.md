# openapi_client.OrgsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_access_token**](OrgsApi.md#create_access_token) | **POST** /orgs/{org_id}/access_tokens | Create organisation access token
[**create_cloudflare_api_key**](OrgsApi.md#create_cloudflare_api_key) | **POST** /orgs/{org_id}/cloudflare | Set CloudFlare API key, org level
[**create_customer**](OrgsApi.md#create_customer) | **POST** /orgs/{org_id}/customers | Create a customer organization
[**create_member**](OrgsApi.md#create_member) | **POST** /orgs/{org_id}/members | Create organization member
[**create_plan**](OrgsApi.md#create_plan) | **POST** /orgs/{org_id}/plans | Create plan
[**create_plan_allowances**](OrgsApi.md#create_plan_allowances) | **POST** /orgs/{org_id}/plans/{plan_id}/allowances | Create plan allowances
[**create_plan_resources**](OrgsApi.md#create_plan_resources) | **POST** /orgs/{org_id}/plans/{plan_id}/resources | Create plan resources
[**create_plan_selections**](OrgsApi.md#create_plan_selections) | **POST** /orgs/{org_id}/plans/{plan_id}/selections | Create plan selections
[**create_tag**](OrgsApi.md#create_tag) | **POST** /orgs/{org_id}/tags | Create tag
[**delete_cloudflare_api_key**](OrgsApi.md#delete_cloudflare_api_key) | **DELETE** /orgs/{org_id}/cloudflare/{cloudflare_key} | Delete CloudFlare API key, org level
[**delete_member**](OrgsApi.md#delete_member) | **DELETE** /orgs/{org_id}/members/{member_id} | Delete organization member
[**delete_org**](OrgsApi.md#delete_org) | **DELETE** /orgs/{org_id} | Delete organization
[**delete_org_avatar**](OrgsApi.md#delete_org_avatar) | **DELETE** /orgs/{org_id}/avatar | Remove org avatar
[**delete_owner**](OrgsApi.md#delete_owner) | **DELETE** /orgs/{org_id}/owner | Delete organization owner
[**delete_plan**](OrgsApi.md#delete_plan) | **DELETE** /orgs/{org_id}/plans/{plan_id} | Delete plan
[**delete_plan_allowance**](OrgsApi.md#delete_plan_allowance) | **DELETE** /orgs/{org_id}/plans/{plan_id}/allowances/{name} | Delete plan allowance
[**delete_website_my_sql_user_access_hosts**](OrgsApi.md#delete_website_my_sql_user_access_hosts) | **DELETE** /orgs/{org_id}/websites/{website_id}/mysql-users/{user_id}/access-hosts | Delete website MySQL database user access hosts
[**get_cloud_flare_key_affected_domains**](OrgsApi.md#get_cloud_flare_key_affected_domains) | **GET** /orgs/{org_id}/cloudflare/{cloudflare_key} | Get affected domains for a CloudFlare key
[**get_cloudflare_api_keys**](OrgsApi.md#get_cloudflare_api_keys) | **GET** /orgs/{org_id}/cloudflare | Get CloudFlare API keys, org level
[**get_customers_added**](OrgsApi.md#get_customers_added) | **GET** /orgs/{org_id}/stats/customers/added | Get customers added over a given time period
[**get_emails**](OrgsApi.md#get_emails) | **GET** /orgs/{org_id}/emails | Get org emails
[**get_member**](OrgsApi.md#get_member) | **GET** /orgs/{org_id}/members/{member_id} | Get organization member
[**get_members**](OrgsApi.md#get_members) | **GET** /orgs/{org_id}/members | Get organization members
[**get_org**](OrgsApi.md#get_org) | **GET** /orgs/{org_id} | Get organization info
[**get_org_activities**](OrgsApi.md#get_org_activities) | **GET** /v2/orgs/{org_id}/activities | Get organization&#39;s activity log.
[**get_org_member_login**](OrgsApi.md#get_org_member_login) | **GET** /orgs/{org_id}/members/{member_id}/sso | Get a One-Time-Password link for the member
[**get_plan**](OrgsApi.md#get_plan) | **GET** /orgs/{org_id}/plans/{plan_id} | Get plan
[**get_plans**](OrgsApi.md#get_plans) | **GET** /orgs/{org_id}/plans | Get plans
[**get_tags**](OrgsApi.md#get_tags) | **GET** /orgs/{org_id}/tags | Get tags
[**get_website_domain_ssl_cert**](OrgsApi.md#get_website_domain_ssl_cert) | **GET** /v2/domains/{domain_id}/ssl | Returns the SSL for this website domain
[**get_website_mail_domain_ssl_cert**](OrgsApi.md#get_website_mail_domain_ssl_cert) | **GET** /v2/domains/{domain_id}/mail_ssl | Returns the SSL for this website domain with the mail.prefix
[**get_websites_added**](OrgsApi.md#get_websites_added) | **GET** /orgs/{org_id}/stats/websites/added | Get websites added over a given time period
[**set_org_avatar**](OrgsApi.md#set_org_avatar) | **PUT** /orgs/{org_id}/avatar | Set org avatar
[**set_website_domain_force_ssl**](OrgsApi.md#set_website_domain_force_ssl) | **PUT** /v2/domains/{domain_id}/ssl/force_ssl | Set \&quot;force ssl\&quot; status for domain mapping
[**update_cloudflare_api_key**](OrgsApi.md#update_cloudflare_api_key) | **PUT** /orgs/{org_id}/cloudflare/{cloudflare_key} | Update CloudFlare API key
[**update_member**](OrgsApi.md#update_member) | **PUT** /orgs/{org_id}/members/{member_id} | Overwrite organization member settings
[**update_org**](OrgsApi.md#update_org) | **PATCH** /orgs/{org_id} | Update organization
[**update_owner**](OrgsApi.md#update_owner) | **PUT** /orgs/{org_id}/owner | Update organization owner
[**update_plan**](OrgsApi.md#update_plan) | **PATCH** /orgs/{org_id}/plans/{plan_id} | Update plan name
[**update_plan_allowance**](OrgsApi.md#update_plan_allowance) | **PUT** /orgs/{org_id}/plans/{plan_id}/allowances/{name} | Update plan allowance
[**update_plan_resource**](OrgsApi.md#update_plan_resource) | **PUT** /orgs/{org_id}/plans/{plan_id}/resources/{name} | Update plan resource
[**update_plan_selection**](OrgsApi.md#update_plan_selection) | **PUT** /orgs/{org_id}/plans/{plan_id}/selections/{name} | Update plan selection
[**upload_website_domain_ssl_cert**](OrgsApi.md#upload_website_domain_ssl_cert) | **POST** /v2/domains/{domain_id}/ssl | Upload custom ssl certificate, key and optional fullchain for a given website
[**upload_website_mail_domain_ssl_cert**](OrgsApi.md#upload_website_mail_domain_ssl_cert) | **POST** /v2/domains/{domain_id}/mail_ssl | Upload SSL for mail.customerdomain.


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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    new_access_token = openapi_client.NewAccessToken() # NewAccessToken | Access token details

    try:
        # Create organisation access token
        api_response = api_instance.create_access_token(org_id, new_access_token)
        print("The response of OrgsApi->create_access_token:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrgsApi->create_access_token: %s\n" % e)
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

# **create_cloudflare_api_key**
> str create_cloudflare_api_key(org_id, new_cloud_flare_token)

Set CloudFlare API key, org level

Adds a CloudFlare API key for an org.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_cloud_flare_token import NewCloudFlareToken
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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    new_cloud_flare_token = openapi_client.NewCloudFlareToken() # NewCloudFlareToken | Key in plain text.

    try:
        # Set CloudFlare API key, org level
        api_response = api_instance.create_cloudflare_api_key(org_id, new_cloud_flare_token)
        print("The response of OrgsApi->create_cloudflare_api_key:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrgsApi->create_cloudflare_api_key: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **new_cloud_flare_token** | [**NewCloudFlareToken**](NewCloudFlareToken.md)| Key in plain text. | 

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
**201** | CloudFlare API key created |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_customer**
> NewResourceUuid create_customer(org_id, new_customer)

Create a customer organization

Once customer is successfully created under parent organization (identified by org_id), the customer organization's id is returned. This operation can only be done by a logged in superadmin or owner of the organization or its parent organization(s).

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_customer import NewCustomer
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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    new_customer = openapi_client.NewCustomer() # NewCustomer | Customer organization details.

    try:
        # Create a customer organization
        api_response = api_instance.create_customer(org_id, new_customer)
        print("The response of OrgsApi->create_customer:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrgsApi->create_customer: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **new_customer** | [**NewCustomer**](NewCustomer.md)| Customer organization details. | 

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
**201** | Customer successfully created |  -  |
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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    new_member = openapi_client.NewMember() # NewMember | New member details

    try:
        # Create organization member
        api_response = api_instance.create_member(org_id, new_member)
        print("The response of OrgsApi->create_member:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrgsApi->create_member: %s\n" % e)
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

# **create_plan**
> NewResourceId create_plan(org_id, new_plan)

Create plan

Creates a new plan for organization. If the organization is a reseller and not the MO, the reseller must itself have a subscription to a reseller plan. It is verified that the reseller is not trying to create a plan offering more resources than the reseller has available through its reseller plan. Session holder must be at least a `SuperAdmin` in this org or a parent org.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_plan import NewPlan
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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    new_plan = openapi_client.NewPlan() # NewPlan | New plan details

    try:
        # Create plan
        api_response = api_instance.create_plan(org_id, new_plan)
        print("The response of OrgsApi->create_plan:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrgsApi->create_plan: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **new_plan** | [**NewPlan**](NewPlan.md)| New plan details | 

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
**201** | Plan successfully created |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |
**409** | Already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_plan_allowances**
> create_plan_allowances(org_id, plan_id, allowance)

Create plan allowances

Creates new allowances for plan. If the organization is a reseller and not the MO, it is verified that the reseller is not trying to update a plan to offer allowances that the reseller doesn't have available in their reseller subscription. Session holder must be at least a `SuperAdmin` in this org or a parent org.

### Example


```python
import openapi_client
from openapi_client.models.allowance import Allowance
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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    plan_id = 56 # int | The id of the plan.
    allowance = [openapi_client.Allowance()] # List[Allowance] | 

    try:
        # Create plan allowances
        api_instance.create_plan_allowances(org_id, plan_id, allowance)
    except Exception as e:
        print("Exception when calling OrgsApi->create_plan_allowances: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **plan_id** | **int**| The id of the plan. | 
 **allowance** | [**List[Allowance]**](Allowance.md)|  | 

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
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_plan_resources**
> create_plan_resources(org_id, plan_id, resource)

Create plan resources

Creates new resources for plan. If the organization is a reseller and not the MO, it is verified that the reseller is not trying to update a plan to offer more of resource than the reseller has available through its reseller subscription. Session holder must be at least a `SuperAdmin` in this org or a parent org.

### Example


```python
import openapi_client
from openapi_client.models.resource import Resource
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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    plan_id = 56 # int | The id of the plan.
    resource = [openapi_client.Resource()] # List[Resource] | 

    try:
        # Create plan resources
        api_instance.create_plan_resources(org_id, plan_id, resource)
    except Exception as e:
        print("Exception when calling OrgsApi->create_plan_resources: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **plan_id** | **int**| The id of the plan. | 
 **resource** | [**List[Resource]**](Resource.md)|  | 

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
**404** | Not found |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**409** | Already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_plan_selections**
> create_plan_selections(org_id, plan_id, selection)

Create plan selections

Creates new selections for plan. If the organization is a reseller and not the MO, it is verified that the reseller is not trying to update a plan to offer selections that the reseller doesn't have available in their reseller subscription. Session holder must be at least a `SuperAdmin` in this org or a parent org.

### Example


```python
import openapi_client
from openapi_client.models.selection import Selection
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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    plan_id = 56 # int | The id of the plan.
    selection = [openapi_client.Selection()] # List[Selection] | 

    try:
        # Create plan selections
        api_instance.create_plan_selections(org_id, plan_id, selection)
    except Exception as e:
        print("Exception when calling OrgsApi->create_plan_selections: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **plan_id** | **int**| The id of the plan. | 
 **selection** | [**List[Selection]**](Selection.md)|  | 

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
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_tag**
> NewResourceId create_tag(org_id, new_tag)

Create tag

Creates a new tag for the organization. Session holder must be at least a `SuperAdmin` in this org or a parent org.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_resource_id import NewResourceId
from openapi_client.models.new_tag import NewTag
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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    new_tag = openapi_client.NewTag() # NewTag | New tag details

    try:
        # Create tag
        api_response = api_instance.create_tag(org_id, new_tag)
        print("The response of OrgsApi->create_tag:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrgsApi->create_tag: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **new_tag** | [**NewTag**](NewTag.md)| New tag details | 

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
**201** | Tag successfully created |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_cloudflare_api_key**
> delete_cloudflare_api_key(org_id, cloudflare_key)

Delete CloudFlare API key, org level

Delete a CloudFlare API key for an org.

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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    cloudflare_key = 'cloudflare_key_example' # str | The id of a CloudFlare key to be acted upon.

    try:
        # Delete CloudFlare API key, org level
        api_instance.delete_cloudflare_api_key(org_id, cloudflare_key)
    except Exception as e:
        print("Exception when calling OrgsApi->delete_cloudflare_api_key: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **cloudflare_key** | **str**| The id of a CloudFlare key to be acted upon. | 

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
**204** | CloudFlare key deleted |  -  |
**400** | Invalid input |  -  |
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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    member_id = 'member_id_example' # str | The id of the member.

    try:
        # Delete organization member
        api_instance.delete_member(org_id, member_id)
    except Exception as e:
        print("Exception when calling OrgsApi->delete_member: %s\n" % e)
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

# **delete_org**
> delete_org(org_id, force=force)

Delete organization

Soft or force deletes the organization and its resources. All resources under the organization (websites, customers in case of a reseller) will be deleted too. If the organization is soft-deleted (or marked as deleted), its data is not removed.  For removing all data and metadata, pass the `force=true` query parameter. This can only be done by a privileged MO member. In this case, all data is wiped, so use carefully. If the `force` parameter is set, session holder must be an MO Owner, SuperAdmin, or Support member, otherwise it suffices for them to be such a member in a parent org.

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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    force = False # bool |  (optional) (default to False)

    try:
        # Delete organization
        api_instance.delete_org(org_id, force=force)
    except Exception as e:
        print("Exception when calling OrgsApi->delete_org: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **force** | **bool**|  | [optional] [default to False]

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
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_org_avatar**
> delete_org_avatar(org_id)

Remove org avatar

Deletes the org's avatar. Session holder must be at least a `SuperAdmin` in this org or a parent org.

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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.

    try:
        # Remove org avatar
        api_instance.delete_org_avatar(org_id)
    except Exception as e:
        print("Exception when calling OrgsApi->delete_org_avatar: %s\n" % e)
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
**204** | Successful |  -  |
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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.

    try:
        # Delete organization owner
        api_instance.delete_owner(org_id)
    except Exception as e:
        print("Exception when calling OrgsApi->delete_owner: %s\n" % e)
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

# **delete_plan**
> delete_plan(org_id, plan_id)

Delete plan

Deletes a plan if no subscriptions exist to it. Session holder must be at least a `SuperAdmin` in this org or a parent org.

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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    plan_id = 56 # int | The id of the plan.

    try:
        # Delete plan
        api_instance.delete_plan(org_id, plan_id)
    except Exception as e:
        print("Exception when calling OrgsApi->delete_plan: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **plan_id** | **int**| The id of the plan. | 

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
**204** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_plan_allowance**
> delete_plan_allowance(org_id, plan_id, name)

Delete plan allowance

Deletes the plan allowance. Session holder must have admin privileges in this org or a parent. That is, to have Owner or SuperAdmin roles in the current org or a parent, or to have the Support role in a parent. org.

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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    plan_id = 56 # int | The id of the plan.
    name = 'name_example' # str | The name of the allowance.

    try:
        # Delete plan allowance
        api_instance.delete_plan_allowance(org_id, plan_id, name)
    except Exception as e:
        print("Exception when calling OrgsApi->delete_plan_allowance: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **plan_id** | **int**| The id of the plan. | 
 **name** | **str**| The name of the allowance. | 

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
**204** | Successful |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_website_my_sql_user_access_hosts**
> delete_website_my_sql_user_access_hosts(org_id, website_id, db_id, user_id, my_sql_user_access_hosts)

Delete website MySQL database user access hosts

Removes from the given user access hosts to website's MySQL database. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.my_sql_user_access_hosts import MySQLUserAccessHosts
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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    db_id = 'db_id_example' # str | The id of the database.
    user_id = 'user_id_example' # str | The id of the database user.
    my_sql_user_access_hosts = openapi_client.MySQLUserAccessHosts() # MySQLUserAccessHosts | User access hosts.

    try:
        # Delete website MySQL database user access hosts
        api_instance.delete_website_my_sql_user_access_hosts(org_id, website_id, db_id, user_id, my_sql_user_access_hosts)
    except Exception as e:
        print("Exception when calling OrgsApi->delete_website_my_sql_user_access_hosts: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **db_id** | **str**| The id of the database. | 
 **user_id** | **str**| The id of the database user. | 
 **my_sql_user_access_hosts** | [**MySQLUserAccessHosts**](MySQLUserAccessHosts.md)| User access hosts. | 

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
**204** | Database user access hosts successfully deleted |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_cloud_flare_key_affected_domains**
> List[str] get_cloud_flare_key_affected_domains(org_id, cloudflare_key)

Get affected domains for a CloudFlare key

Get affected domains for an organisation's CloudFlare key

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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    cloudflare_key = 'cloudflare_key_example' # str | The id of a CloudFlare key to be acted upon.

    try:
        # Get affected domains for a CloudFlare key
        api_response = api_instance.get_cloud_flare_key_affected_domains(org_id, cloudflare_key)
        print("The response of OrgsApi->get_cloud_flare_key_affected_domains:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrgsApi->get_cloud_flare_key_affected_domains: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **cloudflare_key** | **str**| The id of a CloudFlare key to be acted upon. | 

### Return type

**List[str]**

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Domains listed |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_cloudflare_api_keys**
> List[CloudFlareApiKey] get_cloudflare_api_keys(org_id)

Get CloudFlare API keys, org level

Returns the CloudFlare API keys for an org (obfuscated for security).

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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.

    try:
        # Get CloudFlare API keys, org level
        api_response = api_instance.get_cloudflare_api_keys(org_id)
        print("The response of OrgsApi->get_cloudflare_api_keys:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrgsApi->get_cloudflare_api_keys: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 

### Return type

[**List[CloudFlareApiKey]**](CloudFlareApiKey.md)

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

# **get_customers_added**
> List[ResourceCountByInterval] get_customers_added(org_id, time_interval=time_interval)

Get customers added over a given time period

Returns the number of customers added over a given time period. Includes only direct customers, not customers of customers.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.resource_count_by_interval import ResourceCountByInterval
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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    time_interval = 'time_interval_example' # str |  (optional)

    try:
        # Get customers added over a given time period
        api_response = api_instance.get_customers_added(org_id, time_interval=time_interval)
        print("The response of OrgsApi->get_customers_added:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrgsApi->get_customers_added: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **time_interval** | **str**|  | [optional] 

### Return type

[**List[ResourceCountByInterval]**](ResourceCountByInterval.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Stats successfully queried |  -  |
**400** | Invalid input |  -  |
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
    api_instance = openapi_client.OrgsApi(api_client)
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
        print("The response of OrgsApi->get_emails:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrgsApi->get_emails: %s\n" % e)
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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    member_id = 'member_id_example' # str | The id of the member.

    try:
        # Get organization member
        api_response = api_instance.get_member(org_id, member_id)
        print("The response of OrgsApi->get_member:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrgsApi->get_member: %s\n" % e)
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
    api_instance = openapi_client.OrgsApi(api_client)
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
        print("The response of OrgsApi->get_members:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrgsApi->get_members: %s\n" % e)
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

# **get_org**
> Org get_org(org_id)

Get organization info

Returns basic organization information. Session holder must be at least a `SuperAdmin` in this org or a parent org.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.org import Org
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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.

    try:
        # Get organization info
        api_response = api_instance.get_org(org_id)
        print("The response of OrgsApi->get_org:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrgsApi->get_org: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 

### Return type

[**Org**](Org.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Organization successfully queried |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_org_activities**
> ActivitiesListing get_org_activities(org_id, offset=offset, limit=limit, created_before=created_before, created_after=created_after, activity_kinds=activity_kinds, any_entity_id=any_entity_id, entity_kind=entity_kind, search=search)

Get organization's activity log.

Returns organization's activity log which is a human readable list of events that happened in orchd. Only accessible to Owner, SuperAdmin and Sysadmin.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.activities_listing import ActivitiesListing
from openapi_client.models.activity_kind import ActivityKind
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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    offset = 56 # int | The offset from which to return items. (optional)
    limit = 56 # int | The maximum number of items to return. (optional)
    created_before = '2013-10-20' # date | Only return resources which have been created earlier than provided date. (optional)
    created_after = '2013-10-20' # date | Only return resources which have been created after provided date. (optional)
    activity_kinds = [openapi_client.ActivityKind()] # List[ActivityKind] | Select only activities matching the given kinds. If not provided or provided empty array, all kinds are selected as it makes no sense for an activity to not have a kind. (optional)
    any_entity_id = ['any_entity_id_example'] # List[str] | Filter activities maching any of the provided uuids. Since an activity can have 0 or more entities, providing an empty array is not the same as not providing this parameter. An empty array will match activities with 0 entities, while not providing this parameter will ignore this filter. (optional)
    entity_kind = 'entity_kind_example' # str | Activities which contain the given entity kind either as object or context entity. (optional)
    search = 'search_example' # str | Limit the result set to the resources whose names, partially and case insensitively, match the specified search term. E.g. for websites, this is their domain or tag, for databases the database name, for emails the email address or mailbox name, etc. A website will also be returned if the search term exactly matches the website's uuid. (optional)

    try:
        # Get organization's activity log.
        api_response = api_instance.get_org_activities(org_id, offset=offset, limit=limit, created_before=created_before, created_after=created_after, activity_kinds=activity_kinds, any_entity_id=any_entity_id, entity_kind=entity_kind, search=search)
        print("The response of OrgsApi->get_org_activities:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrgsApi->get_org_activities: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **offset** | **int**| The offset from which to return items. | [optional] 
 **limit** | **int**| The maximum number of items to return. | [optional] 
 **created_before** | **date**| Only return resources which have been created earlier than provided date. | [optional] 
 **created_after** | **date**| Only return resources which have been created after provided date. | [optional] 
 **activity_kinds** | [**List[ActivityKind]**](ActivityKind.md)| Select only activities matching the given kinds. If not provided or provided empty array, all kinds are selected as it makes no sense for an activity to not have a kind. | [optional] 
 **any_entity_id** | [**List[str]**](str.md)| Filter activities maching any of the provided uuids. Since an activity can have 0 or more entities, providing an empty array is not the same as not providing this parameter. An empty array will match activities with 0 entities, while not providing this parameter will ignore this filter. | [optional] 
 **entity_kind** | **str**| Activities which contain the given entity kind either as object or context entity. | [optional] 
 **search** | **str**| Limit the result set to the resources whose names, partially and case insensitively, match the specified search term. E.g. for websites, this is their domain or tag, for databases the database name, for emails the email address or mailbox name, etc. A website will also be returned if the search term exactly matches the website&#39;s uuid. | [optional] 

### Return type

[**ActivitiesListing**](ActivitiesListing.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successfully queried |  -  |
**400** | Invalid input |  -  |
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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    member_id = 'member_id_example' # str | The id of the member.

    try:
        # Get a One-Time-Password link for the member
        api_response = api_instance.get_org_member_login(org_id, member_id)
        print("The response of OrgsApi->get_org_member_login:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrgsApi->get_org_member_login: %s\n" % e)
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

# **get_plan**
> Plan get_plan(org_id, plan_id)

Get plan

Returns info on a single plan offered by this organization. Note that the endpoint does not require authentication as anyone should be able to view an organization's plans on offer so that the viewer may decide to subscribe to a plan.

### Example


```python
import openapi_client
from openapi_client.models.plan import Plan
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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    plan_id = 56 # int | The id of the plan.

    try:
        # Get plan
        api_response = api_instance.get_plan(org_id, plan_id)
        print("The response of OrgsApi->get_plan:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrgsApi->get_plan: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **plan_id** | **int**| The id of the plan. | 

### Return type

[**Plan**](Plan.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Organization/plan not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_plans**
> PlansListing get_plans(org_id, offset=offset, limit=limit, sort_by=sort_by, sort_order=sort_order)

Get plans

Returns the organization's plans, optionally filtered by query parameters. Note that the endpoint does not require authentication as anyone should be able to view an organization's plans on offer so that the viewer may decide to subscribe to a plan.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.plans_listing import PlansListing
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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    offset = 56 # int | The offset from which to return items. (optional)
    limit = 56 # int | The maximum number of items to return. (optional)
    sort_by = 'sort_by_example' # str | The field by which to sort. (optional)
    sort_order = 'sort_order_example' # str | The direction in which to sort. Possible values are 'asc' and 'desc', defaulting to 'asc'. (optional)

    try:
        # Get plans
        api_response = api_instance.get_plans(org_id, offset=offset, limit=limit, sort_by=sort_by, sort_order=sort_order)
        print("The response of OrgsApi->get_plans:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrgsApi->get_plans: %s\n" % e)
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

[**PlansListing**](PlansListing.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Organization plans successfully queried |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_tags**
> TagsFullListing get_tags(org_id)

Get tags

Returns all tags belonging to the organization. Session holder must be at least a `SuperAdmin` in this org or a parent org.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.tags_full_listing import TagsFullListing
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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.

    try:
        # Get tags
        api_response = api_instance.get_tags(org_id)
        print("The response of OrgsApi->get_tags:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrgsApi->get_tags: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 

### Return type

[**TagsFullListing**](TagsFullListing.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Organization tags successfully queried |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_domain_ssl_cert**
> DomainSslCertWithData get_website_domain_ssl_cert(domain_id)

Returns the SSL for this website domain

Endpoint for retrieving SSL certificates for a given website including certificates generated by letsencrypt

### Example


```python
import openapi_client
from openapi_client.models.domain_ssl_cert_with_data import DomainSslCertWithData
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
    api_instance = openapi_client.OrgsApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Returns the SSL for this website domain
        api_response = api_instance.get_website_domain_ssl_cert(domain_id)
        print("The response of OrgsApi->get_website_domain_ssl_cert:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrgsApi->get_website_domain_ssl_cert: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 

### Return type

[**DomainSslCertWithData**](DomainSslCertWithData.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | SSL details |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_mail_domain_ssl_cert**
> DomainSslCertWithData get_website_mail_domain_ssl_cert(domain_id)

Returns the SSL for this website domain with the mail.prefix

Endpoint for retrieving SSL certificates for a given website including certificates generated by letsencrypt

### Example


```python
import openapi_client
from openapi_client.models.domain_ssl_cert_with_data import DomainSslCertWithData
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
    api_instance = openapi_client.OrgsApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.

    try:
        # Returns the SSL for this website domain with the mail.prefix
        api_response = api_instance.get_website_mail_domain_ssl_cert(domain_id)
        print("The response of OrgsApi->get_website_mail_domain_ssl_cert:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrgsApi->get_website_mail_domain_ssl_cert: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 

### Return type

[**DomainSslCertWithData**](DomainSslCertWithData.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | SSL details |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_websites_added**
> List[ResourceCountByInterval] get_websites_added(org_id, time_interval=time_interval, recursion=recursion)

Get websites added over a given time period

Returns the number of websites added each day over a given timeframe.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.resource_count_by_interval import ResourceCountByInterval
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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    time_interval = 'time_interval_example' # str |  (optional)
    recursion = True # bool |  (optional)

    try:
        # Get websites added over a given time period
        api_response = api_instance.get_websites_added(org_id, time_interval=time_interval, recursion=recursion)
        print("The response of OrgsApi->get_websites_added:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrgsApi->get_websites_added: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **time_interval** | **str**|  | [optional] 
 **recursion** | **bool**|  | [optional] 

### Return type

[**List[ResourceCountByInterval]**](ResourceCountByInterval.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Stats successfully queried |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_org_avatar**
> set_org_avatar(org_id, avatar)

Set org avatar

Sets the org's avatar, overwriting any previous one if one exists. The max allowed size is 200 KiB. The image format may be jpeg, png, and ico. Session holder must be at least a `SuperAdmin` in this org or a parent org.

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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    avatar = None # bytearray | 

    try:
        # Set org avatar
        api_instance.set_org_avatar(org_id, avatar)
    except Exception as e:
        print("Exception when calling OrgsApi->set_org_avatar: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **avatar** | **bytearray**|  | 

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
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_website_domain_force_ssl**
> set_website_domain_force_ssl(domain_id, body)

Set \"force ssl\" status for domain mapping

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
    api_instance = openapi_client.OrgsApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.
    body = True # bool | Boolean \"force ssl\" setting

    try:
        # Set \"force ssl\" status for domain mapping
        api_instance.set_website_domain_force_ssl(domain_id, body)
    except Exception as e:
        print("Exception when calling OrgsApi->set_website_domain_force_ssl: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 
 **body** | **bool**| Boolean \&quot;force ssl\&quot; setting | 

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
**201** | Setting updated |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_cloudflare_api_key**
> update_cloudflare_api_key(org_id, cloudflare_key, update_cloud_flare_api_key)

Update CloudFlare API key

Update a CloudFlare API key for an org.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.update_cloud_flare_api_key import UpdateCloudFlareApiKey
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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    cloudflare_key = 'cloudflare_key_example' # str | The id of a CloudFlare key to be acted upon.
    update_cloud_flare_api_key = openapi_client.UpdateCloudFlareApiKey() # UpdateCloudFlareApiKey | Key in plain text.

    try:
        # Update CloudFlare API key
        api_instance.update_cloudflare_api_key(org_id, cloudflare_key, update_cloud_flare_api_key)
    except Exception as e:
        print("Exception when calling OrgsApi->update_cloudflare_api_key: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **cloudflare_key** | **str**| The id of a CloudFlare key to be acted upon. | 
 **update_cloud_flare_api_key** | [**UpdateCloudFlareApiKey**](UpdateCloudFlareApiKey.md)| Key in plain text. | 

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
**204** | CloudFlare key deleted |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    member_id = 'member_id_example' # str | The id of the member.
    update_member = openapi_client.UpdateMember() # UpdateMember | Member settings

    try:
        # Overwrite organization member settings
        api_instance.update_member(org_id, member_id, update_member)
    except Exception as e:
        print("Exception when calling OrgsApi->update_member: %s\n" % e)
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

# **update_org**
> update_org(org_id, org_update)

Update organization

Updates the given org's name. Session holder must be at least a `SuperAdmin` in this org or a parent org.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.org_update import OrgUpdate
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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    org_update = openapi_client.OrgUpdate() # OrgUpdate | Organization details.

    try:
        # Update organization
        api_instance.update_org(org_id, org_update)
    except Exception as e:
        print("Exception when calling OrgsApi->update_org: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **org_update** | [**OrgUpdate**](OrgUpdate.md)| Organization details. | 

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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    org_owner_update = openapi_client.OrgOwnerUpdate() # OrgOwnerUpdate | Membership id of the to-be owner

    try:
        # Update organization owner
        api_instance.update_owner(org_id, org_owner_update)
    except Exception as e:
        print("Exception when calling OrgsApi->update_owner: %s\n" % e)
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

# **update_plan**
> update_plan(org_id, plan_id, update_plan)

Update plan name

Updates a plan's name of plan type Session holder must be at least a `SuperAdmin` in this org or a parent org.

### Example


```python
import openapi_client
from openapi_client.models.update_plan import UpdatePlan
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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    plan_id = 56 # int | The id of the plan.
    update_plan = openapi_client.UpdatePlan() # UpdatePlan | 

    try:
        # Update plan name
        api_instance.update_plan(org_id, plan_id, update_plan)
    except Exception as e:
        print("Exception when calling OrgsApi->update_plan: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **plan_id** | **int**| The id of the plan. | 
 **update_plan** | [**UpdatePlan**](UpdatePlan.md)|  | 

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
**204** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_plan_allowance**
> update_plan_allowance(org_id, plan_id, name, allowance)

Update plan allowance

Updates the plan allowance. If the organization is a reseller and not the MO, it is verified that the reseller is not trying to update a plan to offer more of allowance than the reseller has available through its reseller subscription. Session holder must be at least a `SuperAdmin` in this org or a parent org.

### Example


```python
import openapi_client
from openapi_client.models.allowance import Allowance
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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    plan_id = 56 # int | The id of the plan.
    name = 'name_example' # str | The name of the allowance.
    allowance = openapi_client.Allowance() # Allowance | 

    try:
        # Update plan allowance
        api_instance.update_plan_allowance(org_id, plan_id, name, allowance)
    except Exception as e:
        print("Exception when calling OrgsApi->update_plan_allowance: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **plan_id** | **int**| The id of the plan. | 
 **name** | **str**| The name of the allowance. | 
 **allowance** | [**Allowance**](Allowance.md)|  | 

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
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_plan_resource**
> update_plan_resource(org_id, plan_id, name, resource)

Update plan resource

Updates the plan resource. If the organization is a reseller and not the MO, it is verified that the reseller is not trying to update a plan to offer more of resource than the reseller has available through its reseller subscription. Session holder must be at least a `SuperAdmin` in this org or a parent org.

### Example


```python
import openapi_client
from openapi_client.models.resource import Resource
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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    plan_id = 56 # int | The id of the plan.
    name = 'name_example' # str | The name of the resource.
    resource = openapi_client.Resource() # Resource | 

    try:
        # Update plan resource
        api_instance.update_plan_resource(org_id, plan_id, name, resource)
    except Exception as e:
        print("Exception when calling OrgsApi->update_plan_resource: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **plan_id** | **int**| The id of the plan. | 
 **name** | **str**| The name of the resource. | 
 **resource** | [**Resource**](Resource.md)|  | 

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
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_plan_selection**
> update_plan_selection(org_id, plan_id, name, selection)

Update plan selection

Updates the plan selection. If the organization is a reseller and not the MO, it is verified that the reseller is not trying to update a plan to offer more of selection than the reseller has available through its reseller subscription. Session holder must be at least a `SuperAdmin` in this org or a parent org.

### Example


```python
import openapi_client
from openapi_client.models.selection import Selection
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
    api_instance = openapi_client.OrgsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    plan_id = 56 # int | The id of the plan.
    name = 'name_example' # str | The name of the selection.
    selection = openapi_client.Selection() # Selection | 

    try:
        # Update plan selection
        api_instance.update_plan_selection(org_id, plan_id, name, selection)
    except Exception as e:
        print("Exception when calling OrgsApi->update_plan_selection: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **plan_id** | **int**| The id of the plan. | 
 **name** | **str**| The name of the selection. | 
 **selection** | [**Selection**](Selection.md)|  | 

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
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upload_website_domain_ssl_cert**
> NewSslCert upload_website_domain_ssl_cert(domain_id, ssl_cert)

Upload custom ssl certificate, key and optional fullchain for a given website

Endpoint for uploading custom SSL certificate for a given website. Verifies the cert key and maps to relevant domains that the certificate can be applied to. Returns error if no domain match is found. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.new_ssl_cert import NewSslCert
from openapi_client.models.ssl_cert import SslCert
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
    api_instance = openapi_client.OrgsApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.
    ssl_cert = openapi_client.SslCert() # SslCert | Cert, private key and optional fullchain.

    try:
        # Upload custom ssl certificate, key and optional fullchain for a given website
        api_response = api_instance.upload_website_domain_ssl_cert(domain_id, ssl_cert)
        print("The response of OrgsApi->upload_website_domain_ssl_cert:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrgsApi->upload_website_domain_ssl_cert: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 
 **ssl_cert** | [**SslCert**](SslCert.md)| Cert, private key and optional fullchain. | 

### Return type

[**NewSslCert**](NewSslCert.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | SSL Cert successfully uploaded, returns list of applicable domains |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upload_website_mail_domain_ssl_cert**
> NewSslCert upload_website_mail_domain_ssl_cert(domain_id, ssl_cert)

Upload SSL for mail.customerdomain.

### Example


```python
import openapi_client
from openapi_client.models.new_ssl_cert import NewSslCert
from openapi_client.models.ssl_cert import SslCert
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
    api_instance = openapi_client.OrgsApi(api_client)
    domain_id = 'domain_id_example' # str | The id of the domain.
    ssl_cert = openapi_client.SslCert() # SslCert | Cert, private key and optional fullchain.

    try:
        # Upload SSL for mail.customerdomain.
        api_response = api_instance.upload_website_mail_domain_ssl_cert(domain_id, ssl_cert)
        print("The response of OrgsApi->upload_website_mail_domain_ssl_cert:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrgsApi->upload_website_mail_domain_ssl_cert: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The id of the domain. | 
 **ssl_cert** | [**SslCert**](SslCert.md)| Cert, private key and optional fullchain. | 

### Return type

[**NewSslCert**](NewSslCert.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | SSL Cert successfully uploaded |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

