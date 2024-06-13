# openapi_client.LicenceApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_licence_info**](LicenceApi.md#get_licence_info) | **GET** /licence | Get current licence status
[**refresh_licence**](LicenceApi.md#refresh_licence) | **PUT** /licence | Updates licence key if provided, and refresh licence status by calling home servers. NOTE: calling without any licence_key body, only refreshes the current licence status


# **get_licence_info**
> LicenceInfo get_licence_info()

Get current licence status

### Example


```python
import openapi_client
from openapi_client.models.licence_info import LicenceInfo
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
    api_instance = openapi_client.LicenceApi(api_client)

    try:
        # Get current licence status
        api_response = api_instance.get_licence_info()
        print("The response of LicenceApi->get_licence_info:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LicenceApi->get_licence_info: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**LicenceInfo**](LicenceInfo.md)

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

# **refresh_licence**
> LicenceInfo refresh_licence(licence_key=licence_key)

Updates licence key if provided, and refresh licence status by calling home servers. NOTE: calling without any licence_key body, only refreshes the current licence status

### Example


```python
import openapi_client
from openapi_client.models.licence_info import LicenceInfo
from openapi_client.models.licence_key import LicenceKey
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
    api_instance = openapi_client.LicenceApi(api_client)
    licence_key = openapi_client.LicenceKey() # LicenceKey |  (optional)

    try:
        # Updates licence key if provided, and refresh licence status by calling home servers. NOTE: calling without any licence_key body, only refreshes the current licence status
        api_response = api_instance.refresh_licence(licence_key=licence_key)
        print("The response of LicenceApi->refresh_licence:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LicenceApi->refresh_licence: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **licence_key** | [**LicenceKey**](LicenceKey.md)|  | [optional] 

### Return type

[**LicenceInfo**](LicenceInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

