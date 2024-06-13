# openapi_client.CustomersApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_customer**](CustomersApi.md#create_customer) | **POST** /orgs/{org_id}/customers | Create a customer organization
[**create_customer_subscription**](CustomersApi.md#create_customer_subscription) | **POST** /orgs/{org_id}/customers/{customer_org_id}/subscriptions | Create a subscriptions for a customer
[**get_customer_subscriptions**](CustomersApi.md#get_customer_subscriptions) | **GET** /orgs/{org_id}/customers/{customer_org_id}/subscriptions | Get customer subscriptions
[**get_org_customers**](CustomersApi.md#get_org_customers) | **GET** /orgs/{org_id}/customers | Get organization customers


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
    api_instance = openapi_client.CustomersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    new_customer = openapi_client.NewCustomer() # NewCustomer | Customer organization details.

    try:
        # Create a customer organization
        api_response = api_instance.create_customer(org_id, new_customer)
        print("The response of CustomersApi->create_customer:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CustomersApi->create_customer: %s\n" % e)
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

# **create_customer_subscription**
> NewResourceId create_customer_subscription(org_id, customer_org_id, new_subscription)

Create a subscriptions for a customer

Creates a subscription for customer to the org's plan. Only a reseller org or the MO may subscribe another org to one of its plans. If the organization is a reseller (and thus not the MO), it needs to have a suitable subscription to a reseller plan of its parent. It is verified that the reseller's reseller subscription has quota left to create the new subscription (because the new subscription draws from the reseller's reseller subscription). After this call, the sold resources are recorded in the reseller subscription by increasing each sold resource's usage by the sold amount. In combination with the quota check, this is how it is ensured that the reseller doesn't sell more resources than it has paid for. The MO may optionally override the package default servers or server group. All resources of this subscription will then be created on those servers. Otherwise the subscribed to plan's servers are used, or if those aren't defined either, the usual website placement rules are used every time a website is created under this subscription. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_resource_id import NewResourceId
from openapi_client.models.new_subscription import NewSubscription
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
    api_instance = openapi_client.CustomersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    customer_org_id = 'customer_org_id_example' # str | The organization id of the organization's customer.
    new_subscription = openapi_client.NewSubscription() # NewSubscription | Subscription details.

    try:
        # Create a subscriptions for a customer
        api_response = api_instance.create_customer_subscription(org_id, customer_org_id, new_subscription)
        print("The response of CustomersApi->create_customer_subscription:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CustomersApi->create_customer_subscription: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **customer_org_id** | **str**| The organization id of the organization&#39;s customer. | 
 **new_subscription** | [**NewSubscription**](NewSubscription.md)| Subscription details. | 

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
**201** | Subscription successfully created |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |
**409** | Already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_customer_subscriptions**
> SubscriptionsListing get_customer_subscriptions(org_id, customer_org_id, offset=offset, limit=limit, sort_by=sort_by, sort_order=sort_order)

Get customer subscriptions

Lists a customer's subscriptions to packages belonging to the selected organization.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.subscriptions_listing import SubscriptionsListing
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
    api_instance = openapi_client.CustomersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    customer_org_id = 'customer_org_id_example' # str | The organization id of the organization's customer.
    offset = 56 # int | The offset from which to return items. (optional)
    limit = 56 # int | The maximum number of items to return. (optional)
    sort_by = 'sort_by_example' # str | The field by which to sort. (optional)
    sort_order = 'sort_order_example' # str | The direction in which to sort. Possible values are 'asc' and 'desc', defaulting to 'asc'. (optional)

    try:
        # Get customer subscriptions
        api_response = api_instance.get_customer_subscriptions(org_id, customer_org_id, offset=offset, limit=limit, sort_by=sort_by, sort_order=sort_order)
        print("The response of CustomersApi->get_customer_subscriptions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CustomersApi->get_customer_subscriptions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **customer_org_id** | **str**| The organization id of the organization&#39;s customer. | 
 **offset** | **int**| The offset from which to return items. | [optional] 
 **limit** | **int**| The maximum number of items to return. | [optional] 
 **sort_by** | **str**| The field by which to sort. | [optional] 
 **sort_order** | **str**| The direction in which to sort. Possible values are &#39;asc&#39; and &#39;desc&#39;, defaulting to &#39;asc&#39;. | [optional] 

### Return type

[**SubscriptionsListing**](SubscriptionsListing.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Subscriptions successfully queried |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_org_customers**
> CustomersListing get_org_customers(org_id, offset=offset, limit=limit, sort_by=sort_by, sort_order=sort_order, recursive=recursive, max_depth=max_depth, status=status, plan_id=plan_id)

Get organization customers

Returns the list of customers of a reseller organization. If the recursive flag is set, the customers of reseller customers are returned as well recursively, up to an optional max depth value. Note, for performance it is not checked whether org is a reseller. If it is not, an empty list is returned.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.customers_listing import CustomersListing
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
    api_instance = openapi_client.CustomersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    offset = 56 # int | The offset from which to return items. (optional)
    limit = 56 # int | The maximum number of items to return. (optional)
    sort_by = 'sort_by_example' # str | The field by which to sort. (optional)
    sort_order = 'sort_order_example' # str | The direction in which to sort. Possible values are 'asc' and 'desc', defaulting to 'asc'. (optional)
    recursive = True # bool | If set to true, the endpoint will return resources in some hierarchy recursively, that is, several or all levels of the hierarchy, depending on whether `maxDepth` is set. E.g. for customers this means direct and indirect customers are returned. For websites, this returns websites of all direct and indirect customers. (optional)
    max_depth = 56 # int | If recursive is set to true, this can be specified to limit the recursion depth. By default there is no recursion bound. (optional)
    status = 'status_example' # str | Filters the customers list by its status. (optional)
    plan_id = 56 # int | Limit the result set to resources under subscriptions to the plan. (optional)

    try:
        # Get organization customers
        api_response = api_instance.get_org_customers(org_id, offset=offset, limit=limit, sort_by=sort_by, sort_order=sort_order, recursive=recursive, max_depth=max_depth, status=status, plan_id=plan_id)
        print("The response of CustomersApi->get_org_customers:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CustomersApi->get_org_customers: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **offset** | **int**| The offset from which to return items. | [optional] 
 **limit** | **int**| The maximum number of items to return. | [optional] 
 **sort_by** | **str**| The field by which to sort. | [optional] 
 **sort_order** | **str**| The direction in which to sort. Possible values are &#39;asc&#39; and &#39;desc&#39;, defaulting to &#39;asc&#39;. | [optional] 
 **recursive** | **bool**| If set to true, the endpoint will return resources in some hierarchy recursively, that is, several or all levels of the hierarchy, depending on whether &#x60;maxDepth&#x60; is set. E.g. for customers this means direct and indirect customers are returned. For websites, this returns websites of all direct and indirect customers. | [optional] 
 **max_depth** | **int**| If recursive is set to true, this can be specified to limit the recursion depth. By default there is no recursion bound. | [optional] 
 **status** | **str**| Filters the customers list by its status. | [optional] 
 **plan_id** | **int**| Limit the result set to resources under subscriptions to the plan. | [optional] 

### Return type

[**CustomersListing**](CustomersListing.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Customers successfully queried |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

