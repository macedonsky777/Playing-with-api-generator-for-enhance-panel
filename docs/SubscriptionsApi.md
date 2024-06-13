# openapi_client.SubscriptionsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**calculate_resource_usage**](SubscriptionsApi.md#calculate_resource_usage) | **PUT** /orgs/{org_id}/subscriptions/{subscription_id}/calculate-resource-usage | Re-Calculates all subscription resources
[**create_customer_subscription**](SubscriptionsApi.md#create_customer_subscription) | **POST** /orgs/{org_id}/customers/{customer_org_id}/subscriptions | Create a subscriptions for a customer
[**delete_subscription**](SubscriptionsApi.md#delete_subscription) | **DELETE** /orgs/{org_id}/subscriptions/{subscription_id} | Delete subscription
[**get_customer_subscriptions**](SubscriptionsApi.md#get_customer_subscriptions) | **GET** /orgs/{org_id}/customers/{customer_org_id}/subscriptions | Get customer subscriptions
[**get_subscription**](SubscriptionsApi.md#get_subscription) | **GET** /orgs/{org_id}/subscriptions/{subscription_id} | Get subscription
[**get_subscription_bandwidth_usage**](SubscriptionsApi.md#get_subscription_bandwidth_usage) | **GET** /orgs/{org_id}/subscriptions/{subscription_id}/bandwidth | Get subscription bandwidth
[**get_subscriptions_to_parent**](SubscriptionsApi.md#get_subscriptions_to_parent) | **GET** /orgs/{org_id}/subscriptions | Get subscriptions to parent
[**update_subscription**](SubscriptionsApi.md#update_subscription) | **PATCH** /orgs/{org_id}/subscriptions/{subscription_id} | Update subscription


# **calculate_resource_usage**
> UsedResourcesFullListing calculate_resource_usage(org_id, subscription_id)

Re-Calculates all subscription resources

Recursively Re-Calculates organization's subscription resources. Session holder must be at least a `SuperAdmin` in this org or a parent org.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.used_resources_full_listing import UsedResourcesFullListing
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
    api_instance = openapi_client.SubscriptionsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    subscription_id = 3.4 # float | The id of the subscription.

    try:
        # Re-Calculates all subscription resources
        api_response = api_instance.calculate_resource_usage(org_id, subscription_id)
        print("The response of SubscriptionsApi->calculate_resource_usage:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubscriptionsApi->calculate_resource_usage: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **subscription_id** | **float**| The id of the subscription. | 

### Return type

[**UsedResourcesFullListing**](UsedResourcesFullListing.md)

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
    api_instance = openapi_client.SubscriptionsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    customer_org_id = 'customer_org_id_example' # str | The organization id of the organization's customer.
    new_subscription = openapi_client.NewSubscription() # NewSubscription | Subscription details.

    try:
        # Create a subscriptions for a customer
        api_response = api_instance.create_customer_subscription(org_id, customer_org_id, new_subscription)
        print("The response of SubscriptionsApi->create_customer_subscription:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubscriptionsApi->create_customer_subscription: %s\n" % e)
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

# **delete_subscription**
> delete_subscription(org_id, subscription_id, force=force)

Delete subscription

Soft or force deletes the subscription and its resources. All resources under the subscription (websites, customers in case of a reseller) will be deleted too. If the subscription is soft-deleted (or marked as deleted), its data is not removed.  For removing all data and metadata, pass the `force=true` query parameter. This can only be done by a privileged MO member. In this case, all data is wiped, so use carefully. If the `force` parameter is set, session holder must be an MO Owner, SuperAdmin, or Support member, otherwise it suffices for them to be such a member in a parent org.

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
    api_instance = openapi_client.SubscriptionsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    subscription_id = 3.4 # float | The id of the subscription.
    force = False # bool |  (optional) (default to False)

    try:
        # Delete subscription
        api_instance.delete_subscription(org_id, subscription_id, force=force)
    except Exception as e:
        print("Exception when calling SubscriptionsApi->delete_subscription: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **subscription_id** | **float**| The id of the subscription. | 
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
    api_instance = openapi_client.SubscriptionsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    customer_org_id = 'customer_org_id_example' # str | The organization id of the organization's customer.
    offset = 56 # int | The offset from which to return items. (optional)
    limit = 56 # int | The maximum number of items to return. (optional)
    sort_by = 'sort_by_example' # str | The field by which to sort. (optional)
    sort_order = 'sort_order_example' # str | The direction in which to sort. Possible values are 'asc' and 'desc', defaulting to 'asc'. (optional)

    try:
        # Get customer subscriptions
        api_response = api_instance.get_customer_subscriptions(org_id, customer_org_id, offset=offset, limit=limit, sort_by=sort_by, sort_order=sort_order)
        print("The response of SubscriptionsApi->get_customer_subscriptions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubscriptionsApi->get_customer_subscriptions: %s\n" % e)
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

# **get_subscription**
> Subscription get_subscription(org_id, subscription_id)

Get subscription

Queries the organization's subscription. Session holder must be at least a `SuperAdmin` in this org or a parent org.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.subscription import Subscription
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
    api_instance = openapi_client.SubscriptionsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    subscription_id = 3.4 # float | The id of the subscription.

    try:
        # Get subscription
        api_response = api_instance.get_subscription(org_id, subscription_id)
        print("The response of SubscriptionsApi->get_subscription:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubscriptionsApi->get_subscription: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **subscription_id** | **float**| The id of the subscription. | 

### Return type

[**Subscription**](Subscription.md)

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

# **get_subscription_bandwidth_usage**
> int get_subscription_bandwidth_usage(org_id, subscription_id, refresh_cache=refresh_cache)

Get subscription bandwidth

Queries the organization's subscription bandwidth for the current month. This includes all customer subscriptions if this subscription is a reseller. By default the usage is cached for 12 hours unless `refreshCache` is `true`. The value is in bytes. Session holder must be at least a `SuperAdmin` in this org or a parent org.

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
    api_instance = openapi_client.SubscriptionsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    subscription_id = 3.4 # float | The id of the subscription.
    refresh_cache = True # bool | If set to true, it will bypass internal caching. (optional)

    try:
        # Get subscription bandwidth
        api_response = api_instance.get_subscription_bandwidth_usage(org_id, subscription_id, refresh_cache=refresh_cache)
        print("The response of SubscriptionsApi->get_subscription_bandwidth_usage:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubscriptionsApi->get_subscription_bandwidth_usage: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **subscription_id** | **float**| The id of the subscription. | 
 **refresh_cache** | **bool**| If set to true, it will bypass internal caching. | [optional] 

### Return type

**int**

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

# **get_subscriptions_to_parent**
> SubscriptionsListing get_subscriptions_to_parent(org_id, offset=offset, limit=limit, sort_by=sort_by, sort_order=sort_order)

Get subscriptions to parent

Lists subscriptions to the packages of the parent organization to which the currently selected organization is subscribed.

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
    api_instance = openapi_client.SubscriptionsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    offset = 56 # int | The offset from which to return items. (optional)
    limit = 56 # int | The maximum number of items to return. (optional)
    sort_by = 'sort_by_example' # str | The field by which to sort. (optional)
    sort_order = 'sort_order_example' # str | The direction in which to sort. Possible values are 'asc' and 'desc', defaulting to 'asc'. (optional)

    try:
        # Get subscriptions to parent
        api_response = api_instance.get_subscriptions_to_parent(org_id, offset=offset, limit=limit, sort_by=sort_by, sort_order=sort_order)
        print("The response of SubscriptionsApi->get_subscriptions_to_parent:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubscriptionsApi->get_subscriptions_to_parent: %s\n" % e)
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

# **update_subscription**
> update_subscription(org_id, subscription_id, update_subscription)

Update subscription

Updates the organization's subscription. This endpoint is used to update the subscription's status and suspension, by a parent organization admin.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.update_subscription import UpdateSubscription
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
    api_instance = openapi_client.SubscriptionsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    subscription_id = 3.4 # float | The id of the subscription.
    update_subscription = openapi_client.UpdateSubscription() # UpdateSubscription | 

    try:
        # Update subscription
        api_instance.update_subscription(org_id, subscription_id, update_subscription)
    except Exception as e:
        print("Exception when calling SubscriptionsApi->update_subscription: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **subscription_id** | **float**| The id of the subscription. | 
 **update_subscription** | [**UpdateSubscription**](UpdateSubscription.md)|  | 

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

