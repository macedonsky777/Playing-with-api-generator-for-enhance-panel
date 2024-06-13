# openapi_client.AppsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_website_app**](AppsApi.md#create_website_app) | **POST** /orgs/{org_id}/websites/{website_id}/apps | Create website applications
[**delete_website_app**](AppsApi.md#delete_website_app) | **DELETE** /orgs/{org_id}/websites/{website_id}/apps/{app_id} | Delete website app
[**get_global_installable_apps**](AppsApi.md#get_global_installable_apps) | **GET** /utils/installable-apps | Get all installable applications
[**get_installable_apps**](AppsApi.md#get_installable_apps) | **GET** /orgs/{org_id}/subscriptions/{subscription_id}/installable-apps | Get installable website applications
[**get_website_apps**](AppsApi.md#get_website_apps) | **GET** /orgs/{org_id}/websites/{website_id}/apps | Get website applications


# **create_website_app**
> NewResourceUuid create_website_app(org_id, website_id, new_website_app)

Create website applications

Creates a new application for website. Note that if the installed app is WordPress, this endpoint will enable PHP for the website if it isn't already. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.new_resource_uuid import NewResourceUuid
from openapi_client.models.new_website_app import NewWebsiteApp
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
    api_instance = openapi_client.AppsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    new_website_app = openapi_client.NewWebsiteApp() # NewWebsiteApp | 

    try:
        # Create website applications
        api_response = api_instance.create_website_app(org_id, website_id, new_website_app)
        print("The response of AppsApi->create_website_app:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AppsApi->create_website_app: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **new_website_app** | [**NewWebsiteApp**](NewWebsiteApp.md)|  | 

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
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_website_app**
> delete_website_app(org_id, website_id, app_id, backup_before_operation=backup_before_operation)

Delete website app

Deletes an existing website app. Unless `backupBeforeOperation=false` query param is sent, it runs a website backup before deleting the app. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

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
    api_instance = openapi_client.AppsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    app_id = 'app_id_example' # str | The id of the app.
    backup_before_operation = True # bool | Whether a backup should be ran before the endpoint operation is executed. (optional)

    try:
        # Delete website app
        api_instance.delete_website_app(org_id, website_id, app_id, backup_before_operation=backup_before_operation)
    except Exception as e:
        print("Exception when calling AppsApi->delete_website_app: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **app_id** | **str**| The id of the app. | 
 **backup_before_operation** | **bool**| Whether a backup should be ran before the endpoint operation is executed. | [optional] 

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
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_global_installable_apps**
> InstallableWebsiteAppsFullListing get_global_installable_apps()

Get all installable applications

Returns all installable applications. Note that what apps can be installed on a website is ultimately decided by customer's subscription. See operationId `getInstallableApps`.

### Example


```python
import openapi_client
from openapi_client.models.installable_website_apps_full_listing import InstallableWebsiteAppsFullListing
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
    api_instance = openapi_client.AppsApi(api_client)

    try:
        # Get all installable applications
        api_response = api_instance.get_global_installable_apps()
        print("The response of AppsApi->get_global_installable_apps:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AppsApi->get_global_installable_apps: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**InstallableWebsiteAppsFullListing**](InstallableWebsiteAppsFullListing.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_installable_apps**
> InstallableWebsiteAppsFullListing get_installable_apps(org_id, subscription_id)

Get installable website applications

Returns all installable applications under the subscription.

### Example


```python
import openapi_client
from openapi_client.models.installable_website_apps_full_listing import InstallableWebsiteAppsFullListing
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
    api_instance = openapi_client.AppsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    subscription_id = 3.4 # float | The id of the subscription.

    try:
        # Get installable website applications
        api_response = api_instance.get_installable_apps(org_id, subscription_id)
        print("The response of AppsApi->get_installable_apps:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AppsApi->get_installable_apps: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **subscription_id** | **float**| The id of the subscription. | 

### Return type

[**InstallableWebsiteAppsFullListing**](InstallableWebsiteAppsFullListing.md)

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
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_apps**
> WebsiteAppsFullListing get_website_apps(org_id, website_id)

Get website applications

Returns all applications installed on this website. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.website_apps_full_listing import WebsiteAppsFullListing
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
    api_instance = openapi_client.AppsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Get website applications
        api_response = api_instance.get_website_apps(org_id, website_id)
        print("The response of AppsApi->get_website_apps:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AppsApi->get_website_apps: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 

### Return type

[**WebsiteAppsFullListing**](WebsiteAppsFullListing.md)

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
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

