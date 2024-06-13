# openapi_client.PlansApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_plan**](PlansApi.md#create_plan) | **POST** /orgs/{org_id}/plans | Create plan
[**create_plan_allowances**](PlansApi.md#create_plan_allowances) | **POST** /orgs/{org_id}/plans/{plan_id}/allowances | Create plan allowances
[**create_plan_resources**](PlansApi.md#create_plan_resources) | **POST** /orgs/{org_id}/plans/{plan_id}/resources | Create plan resources
[**create_plan_selections**](PlansApi.md#create_plan_selections) | **POST** /orgs/{org_id}/plans/{plan_id}/selections | Create plan selections
[**delete_plan**](PlansApi.md#delete_plan) | **DELETE** /orgs/{org_id}/plans/{plan_id} | Delete plan
[**delete_plan_allowance**](PlansApi.md#delete_plan_allowance) | **DELETE** /orgs/{org_id}/plans/{plan_id}/allowances/{name} | Delete plan allowance
[**get_plan**](PlansApi.md#get_plan) | **GET** /orgs/{org_id}/plans/{plan_id} | Get plan
[**get_plans**](PlansApi.md#get_plans) | **GET** /orgs/{org_id}/plans | Get plans
[**update_plan**](PlansApi.md#update_plan) | **PATCH** /orgs/{org_id}/plans/{plan_id} | Update plan name
[**update_plan_allowance**](PlansApi.md#update_plan_allowance) | **PUT** /orgs/{org_id}/plans/{plan_id}/allowances/{name} | Update plan allowance
[**update_plan_resource**](PlansApi.md#update_plan_resource) | **PUT** /orgs/{org_id}/plans/{plan_id}/resources/{name} | Update plan resource
[**update_plan_selection**](PlansApi.md#update_plan_selection) | **PUT** /orgs/{org_id}/plans/{plan_id}/selections/{name} | Update plan selection


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
    api_instance = openapi_client.PlansApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    new_plan = openapi_client.NewPlan() # NewPlan | New plan details

    try:
        # Create plan
        api_response = api_instance.create_plan(org_id, new_plan)
        print("The response of PlansApi->create_plan:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PlansApi->create_plan: %s\n" % e)
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
    api_instance = openapi_client.PlansApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    plan_id = 56 # int | The id of the plan.
    allowance = [openapi_client.Allowance()] # List[Allowance] | 

    try:
        # Create plan allowances
        api_instance.create_plan_allowances(org_id, plan_id, allowance)
    except Exception as e:
        print("Exception when calling PlansApi->create_plan_allowances: %s\n" % e)
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
    api_instance = openapi_client.PlansApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    plan_id = 56 # int | The id of the plan.
    resource = [openapi_client.Resource()] # List[Resource] | 

    try:
        # Create plan resources
        api_instance.create_plan_resources(org_id, plan_id, resource)
    except Exception as e:
        print("Exception when calling PlansApi->create_plan_resources: %s\n" % e)
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
    api_instance = openapi_client.PlansApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    plan_id = 56 # int | The id of the plan.
    selection = [openapi_client.Selection()] # List[Selection] | 

    try:
        # Create plan selections
        api_instance.create_plan_selections(org_id, plan_id, selection)
    except Exception as e:
        print("Exception when calling PlansApi->create_plan_selections: %s\n" % e)
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
    api_instance = openapi_client.PlansApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    plan_id = 56 # int | The id of the plan.

    try:
        # Delete plan
        api_instance.delete_plan(org_id, plan_id)
    except Exception as e:
        print("Exception when calling PlansApi->delete_plan: %s\n" % e)
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
    api_instance = openapi_client.PlansApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    plan_id = 56 # int | The id of the plan.
    name = 'name_example' # str | The name of the allowance.

    try:
        # Delete plan allowance
        api_instance.delete_plan_allowance(org_id, plan_id, name)
    except Exception as e:
        print("Exception when calling PlansApi->delete_plan_allowance: %s\n" % e)
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
    api_instance = openapi_client.PlansApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    plan_id = 56 # int | The id of the plan.

    try:
        # Get plan
        api_response = api_instance.get_plan(org_id, plan_id)
        print("The response of PlansApi->get_plan:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PlansApi->get_plan: %s\n" % e)
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
    api_instance = openapi_client.PlansApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    offset = 56 # int | The offset from which to return items. (optional)
    limit = 56 # int | The maximum number of items to return. (optional)
    sort_by = 'sort_by_example' # str | The field by which to sort. (optional)
    sort_order = 'sort_order_example' # str | The direction in which to sort. Possible values are 'asc' and 'desc', defaulting to 'asc'. (optional)

    try:
        # Get plans
        api_response = api_instance.get_plans(org_id, offset=offset, limit=limit, sort_by=sort_by, sort_order=sort_order)
        print("The response of PlansApi->get_plans:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PlansApi->get_plans: %s\n" % e)
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
    api_instance = openapi_client.PlansApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    plan_id = 56 # int | The id of the plan.
    update_plan = openapi_client.UpdatePlan() # UpdatePlan | 

    try:
        # Update plan name
        api_instance.update_plan(org_id, plan_id, update_plan)
    except Exception as e:
        print("Exception when calling PlansApi->update_plan: %s\n" % e)
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
    api_instance = openapi_client.PlansApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    plan_id = 56 # int | The id of the plan.
    name = 'name_example' # str | The name of the allowance.
    allowance = openapi_client.Allowance() # Allowance | 

    try:
        # Update plan allowance
        api_instance.update_plan_allowance(org_id, plan_id, name, allowance)
    except Exception as e:
        print("Exception when calling PlansApi->update_plan_allowance: %s\n" % e)
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
    api_instance = openapi_client.PlansApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    plan_id = 56 # int | The id of the plan.
    name = 'name_example' # str | The name of the resource.
    resource = openapi_client.Resource() # Resource | 

    try:
        # Update plan resource
        api_instance.update_plan_resource(org_id, plan_id, name, resource)
    except Exception as e:
        print("Exception when calling PlansApi->update_plan_resource: %s\n" % e)
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
    api_instance = openapi_client.PlansApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    plan_id = 56 # int | The id of the plan.
    name = 'name_example' # str | The name of the selection.
    selection = openapi_client.Selection() # Selection | 

    try:
        # Update plan selection
        api_instance.update_plan_selection(org_id, plan_id, name, selection)
    except Exception as e:
        print("Exception when calling PlansApi->update_plan_selection: %s\n" % e)
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

