# openapi_client.InstallApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**controld_version**](InstallApi.md#controld_version) | **GET** /install/compatible_versions/controld | Get the compatible controld version
[**get_service_kind_latest_version**](InstallApi.md#get_service_kind_latest_version) | **GET** /install/latest_available_version/{service_kind} | Get the latest available version of a given service kind
[**install**](InstallApi.md#install) | **POST** /install | Create the master organization owner
[**orchd_status**](InstallApi.md#orchd_status) | **GET** /status | Get the readiness status of the orchd service
[**orchd_version**](InstallApi.md#orchd_version) | **GET** /version | Get the SemVer of the API service
[**update_enhance**](InstallApi.md#update_enhance) | **POST** /install/update | Updates all services in the cluster.
[**validate_installation**](InstallApi.md#validate_installation) | **POST** /install/validate | Used to validate that the control panel has been initialized.


# **controld_version**
> str controld_version()

Get the compatible controld version

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
    api_instance = openapi_client.InstallApi(api_client)

    try:
        # Get the compatible controld version
        api_response = api_instance.controld_version()
        print("The response of InstallApi->controld_version:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InstallApi->controld_version: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

**str**

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

# **get_service_kind_latest_version**
> str get_service_kind_latest_version(service_kind)

Get the latest available version of a given service kind

Fetches the latest version of a given service kind from the docker repository.  This version can then be installed using updateEnhance

### Example


```python
import openapi_client
from openapi_client.models.service_kind import ServiceKind
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
    api_instance = openapi_client.InstallApi(api_client)
    service_kind = openapi_client.ServiceKind() # ServiceKind | The service type of the role.

    try:
        # Get the latest available version of a given service kind
        api_response = api_instance.get_service_kind_latest_version(service_kind)
        print("The response of InstallApi->get_service_kind_latest_version:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InstallApi->get_service_kind_latest_version: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **service_kind** | [**ServiceKind**](.md)| The service type of the role. | 

### Return type

**str**

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **install**
> SetupResult install(key, install)

Create the master organization owner

Installs the control panel. It creates the master org owner and sets the master org control panel host. This procedure may only be invoked once, when the control panel is first set up. It also authenticates the new login and returns a session token as a convenience step.

### Example


```python
import openapi_client
from openapi_client.models.install import Install
from openapi_client.models.setup_result import SetupResult
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
    api_instance = openapi_client.InstallApi(api_client)
    key = 'key_example' # str | The secret registration key
    install = openapi_client.Install() # Install | Master organization owner details.

    try:
        # Create the master organization owner
        api_response = api_instance.install(key, install)
        print("The response of InstallApi->install:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InstallApi->install: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key** | **str**| The secret registration key | 
 **install** | [**Install**](Install.md)| Master organization owner details. | 

### Return type

[**SetupResult**](SetupResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Install successful |  * Set-Cookie -  <br>  |
**400** | Invalid registration key/input |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **orchd_status**
> str orchd_status()

Get the readiness status of the orchd service

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
    api_instance = openapi_client.InstallApi(api_client)

    try:
        # Get the readiness status of the orchd service
        api_response = api_instance.orchd_status()
        print("The response of InstallApi->orchd_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InstallApi->orchd_status: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

**str**

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

# **orchd_version**
> str orchd_version()

Get the SemVer of the API service

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
    api_instance = openapi_client.InstallApi(api_client)

    try:
        # Get the SemVer of the API service
        api_response = api_instance.orchd_version()
        print("The response of InstallApi->orchd_version:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InstallApi->orchd_version: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

**str**

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

# **update_enhance**
> update_enhance()

Updates all services in the cluster.

Updates the control panel. Checks whether there are any compatible version releases for all deployed services and performs an update if so. This endpoint blocks while the updates are running.

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
    api_instance = openapi_client.InstallApi(api_client)

    try:
        # Updates all services in the cluster.
        api_instance.update_enhance()
    except Exception as e:
        print("Exception when calling InstallApi->update_enhance: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

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
**200** | Successful |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **validate_installation**
> ValidationResult validate_installation()

Used to validate that the control panel has been initialized.

### Example


```python
import openapi_client
from openapi_client.models.validation_result import ValidationResult
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
    api_instance = openapi_client.InstallApi(api_client)

    try:
        # Used to validate that the control panel has been initialized.
        api_response = api_instance.validate_installation()
        print("The response of InstallApi->validate_installation:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InstallApi->validate_installation: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**ValidationResult**](ValidationResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Master org has been set up |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

