# openapi_client.SettingsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_orchd_login_policy_email_blacklist**](SettingsApi.md#add_orchd_login_policy_email_blacklist) | **PUT** /settings/orchd/login-policy/email-blacklist | Set the orchd login policy email blacklist as a whole
[**add_orchd_login_policy_email_whitelist**](SettingsApi.md#add_orchd_login_policy_email_whitelist) | **PUT** /settings/orchd/login-policy/email-whitelist | Set the orchd login policy email whitelist as a whole
[**add_orchd_login_policy_ip_blacklist**](SettingsApi.md#add_orchd_login_policy_ip_blacklist) | **PUT** /settings/orchd/login-policy/ip-blacklist | Set the orchd login policy ip blacklist as a whole
[**add_orchd_login_policy_ip_whitelist**](SettingsApi.md#add_orchd_login_policy_ip_whitelist) | **PUT** /settings/orchd/login-policy/ip-whitelist | Set the orchd login policy ip whitelist as a whole
[**add_orchd_login_policy_settings**](SettingsApi.md#add_orchd_login_policy_settings) | **PUT** /settings/orchd/login-policy/settings | Set a single orchd login policy setting
[**create_backup_remote_storage_s3**](SettingsApi.md#create_backup_remote_storage_s3) | **POST** /v2/settings/backup/remote_storage/s3 | Create S3 object storage settings at platform level.
[**create_settings**](SettingsApi.md#create_settings) | **POST** /settings | Create settings
[**delete_backup_remote_storage_s3**](SettingsApi.md#delete_backup_remote_storage_s3) | **DELETE** /v2/settings/backup/remote_storage/s3 | Delete S3 object storage settings at platform level.
[**delete_global_service_setting**](SettingsApi.md#delete_global_service_setting) | **DELETE** /settings/service/{setting_kind}/{setting_key} | Delete a single global service setting
[**delete_orchd_login_policy_email_blacklist**](SettingsApi.md#delete_orchd_login_policy_email_blacklist) | **DELETE** /settings/orchd/login-policy/email-blacklist | Delete an orchd login policy email blacklist
[**delete_orchd_login_policy_email_whitelist**](SettingsApi.md#delete_orchd_login_policy_email_whitelist) | **DELETE** /settings/orchd/login-policy/email-whitelist | Delete an orchd login policy email whitelist
[**delete_orchd_login_policy_ip_blacklist**](SettingsApi.md#delete_orchd_login_policy_ip_blacklist) | **DELETE** /settings/orchd/login-policy/ip-blacklist | Delete an orchd login policy ip blacklist
[**delete_orchd_login_policy_ip_whitelist**](SettingsApi.md#delete_orchd_login_policy_ip_whitelist) | **DELETE** /settings/orchd/login-policy/ip-whitelist | Delete an orchd login policy ip whitelist
[**delete_setting**](SettingsApi.md#delete_setting) | **DELETE** /settings/{name} | Remove the specified setting
[**get_backup_remote_storage_s3**](SettingsApi.md#get_backup_remote_storage_s3) | **GET** /v2/settings/backup/remote_storage/s3 | Get S3 object storage settings at platform level.
[**get_demo_mode**](SettingsApi.md#get_demo_mode) | **GET** /v2/settings/demo_mode | Get the demo mode status of the orchd service
[**get_docker_registry**](SettingsApi.md#get_docker_registry) | **GET** /settings/registry | Gets the Docker registry credentials.
[**get_global_service_setting**](SettingsApi.md#get_global_service_setting) | **GET** /settings/service/{setting_kind} | Get the value for a particular global service setting
[**get_orchd_log_settings**](SettingsApi.md#get_orchd_log_settings) | **GET** /settings/orchd/logs | Get the orchd log settings
[**get_orchd_login_policy_email_blacklist**](SettingsApi.md#get_orchd_login_policy_email_blacklist) | **GET** /settings/orchd/login-policy/email-blacklist | Get the orchd login policy email blacklist
[**get_orchd_login_policy_email_whitelist**](SettingsApi.md#get_orchd_login_policy_email_whitelist) | **GET** /settings/orchd/login-policy/email-whitelist | Get the orchd login policy email whitelist
[**get_orchd_login_policy_ip_blacklist**](SettingsApi.md#get_orchd_login_policy_ip_blacklist) | **GET** /settings/orchd/login-policy/ip-blacklist | Get the orchd login policy ip blacklist
[**get_orchd_login_policy_ip_whitelist**](SettingsApi.md#get_orchd_login_policy_ip_whitelist) | **GET** /settings/orchd/login-policy/ip-whitelist | Get the orchd login policy ip whitelist
[**get_orchd_login_policy_settings**](SettingsApi.md#get_orchd_login_policy_settings) | **GET** /settings/orchd/login-policy/settings | Get the orchd login policy settings
[**get_prohibited_domains**](SettingsApi.md#get_prohibited_domains) | **GET** /settings/orchd/prohibited_domains | Get the platform level prohibited domains as a newline separated list
[**get_setting**](SettingsApi.md#get_setting) | **GET** /settings/{name} | Get the specified setting
[**get_settings**](SettingsApi.md#get_settings) | **GET** /settings | Get all current settings
[**set_docker_registry**](SettingsApi.md#set_docker_registry) | **PUT** /settings/registry | Updates the Docker registry credentials.
[**set_global_service_setting**](SettingsApi.md#set_global_service_setting) | **PUT** /settings/service/{setting_kind}/{setting_key} | Set a single global service setting
[**set_orchd_log_settings**](SettingsApi.md#set_orchd_log_settings) | **PUT** /settings/orchd/logs | Set the orchd log settings
[**set_prohibited_domains**](SettingsApi.md#set_prohibited_domains) | **PUT** /settings/orchd/prohibited_domains | Set the platform level prohibited domains
[**update_backup_remote_storage_s3**](SettingsApi.md#update_backup_remote_storage_s3) | **PATCH** /v2/settings/backup/remote_storage/s3 | Update S3 object storage settings at platform level.
[**update_setting**](SettingsApi.md#update_setting) | **PUT** /settings/{name} | Create or update the specified setting


# **add_orchd_login_policy_email_blacklist**
> add_orchd_login_policy_email_blacklist(orchd_login_policy_email_list)

Set the orchd login policy email blacklist as a whole

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.orchd_login_policy_email_list import OrchdLoginPolicyEmailList
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
    api_instance = openapi_client.SettingsApi(api_client)
    orchd_login_policy_email_list = openapi_client.OrchdLoginPolicyEmailList() # OrchdLoginPolicyEmailList | 

    try:
        # Set the orchd login policy email blacklist as a whole
        api_instance.add_orchd_login_policy_email_blacklist(orchd_login_policy_email_list)
    except Exception as e:
        print("Exception when calling SettingsApi->add_orchd_login_policy_email_blacklist: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orchd_login_policy_email_list** | [**OrchdLoginPolicyEmailList**](OrchdLoginPolicyEmailList.md)|  | 

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
**400** | Invalid request |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **add_orchd_login_policy_email_whitelist**
> add_orchd_login_policy_email_whitelist(orchd_login_policy_email_list)

Set the orchd login policy email whitelist as a whole

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.orchd_login_policy_email_list import OrchdLoginPolicyEmailList
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
    api_instance = openapi_client.SettingsApi(api_client)
    orchd_login_policy_email_list = openapi_client.OrchdLoginPolicyEmailList() # OrchdLoginPolicyEmailList | 

    try:
        # Set the orchd login policy email whitelist as a whole
        api_instance.add_orchd_login_policy_email_whitelist(orchd_login_policy_email_list)
    except Exception as e:
        print("Exception when calling SettingsApi->add_orchd_login_policy_email_whitelist: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orchd_login_policy_email_list** | [**OrchdLoginPolicyEmailList**](OrchdLoginPolicyEmailList.md)|  | 

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
**400** | Invalid request |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **add_orchd_login_policy_ip_blacklist**
> add_orchd_login_policy_ip_blacklist(orchd_login_policy_ip_list)

Set the orchd login policy ip blacklist as a whole

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.orchd_login_policy_ip_list import OrchdLoginPolicyIpList
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
    api_instance = openapi_client.SettingsApi(api_client)
    orchd_login_policy_ip_list = openapi_client.OrchdLoginPolicyIpList() # OrchdLoginPolicyIpList | 

    try:
        # Set the orchd login policy ip blacklist as a whole
        api_instance.add_orchd_login_policy_ip_blacklist(orchd_login_policy_ip_list)
    except Exception as e:
        print("Exception when calling SettingsApi->add_orchd_login_policy_ip_blacklist: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orchd_login_policy_ip_list** | [**OrchdLoginPolicyIpList**](OrchdLoginPolicyIpList.md)|  | 

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
**400** | Invalid request |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **add_orchd_login_policy_ip_whitelist**
> add_orchd_login_policy_ip_whitelist(orchd_login_policy_ip_list)

Set the orchd login policy ip whitelist as a whole

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.orchd_login_policy_ip_list import OrchdLoginPolicyIpList
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
    api_instance = openapi_client.SettingsApi(api_client)
    orchd_login_policy_ip_list = openapi_client.OrchdLoginPolicyIpList() # OrchdLoginPolicyIpList | 

    try:
        # Set the orchd login policy ip whitelist as a whole
        api_instance.add_orchd_login_policy_ip_whitelist(orchd_login_policy_ip_list)
    except Exception as e:
        print("Exception when calling SettingsApi->add_orchd_login_policy_ip_whitelist: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orchd_login_policy_ip_list** | [**OrchdLoginPolicyIpList**](OrchdLoginPolicyIpList.md)|  | 

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
**400** | Invalid request |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **add_orchd_login_policy_settings**
> add_orchd_login_policy_settings(orchd_login_policy_settings)

Set a single orchd login policy setting

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.orchd_login_policy_settings import OrchdLoginPolicySettings
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
    api_instance = openapi_client.SettingsApi(api_client)
    orchd_login_policy_settings = openapi_client.OrchdLoginPolicySettings() # OrchdLoginPolicySettings | 

    try:
        # Set a single orchd login policy setting
        api_instance.add_orchd_login_policy_settings(orchd_login_policy_settings)
    except Exception as e:
        print("Exception when calling SettingsApi->add_orchd_login_policy_settings: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orchd_login_policy_settings** | [**OrchdLoginPolicySettings**](OrchdLoginPolicySettings.md)|  | 

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
**400** | Invalid request |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_backup_remote_storage_s3**
> create_backup_remote_storage_s3(create_backup_remote_storage_s3)

Create S3 object storage settings at platform level.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.create_backup_remote_storage_s3 import CreateBackupRemoteStorageS3
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
    api_instance = openapi_client.SettingsApi(api_client)
    create_backup_remote_storage_s3 = openapi_client.CreateBackupRemoteStorageS3() # CreateBackupRemoteStorageS3 | 

    try:
        # Create S3 object storage settings at platform level.
        api_instance.create_backup_remote_storage_s3(create_backup_remote_storage_s3)
    except Exception as e:
        print("Exception when calling SettingsApi->create_backup_remote_storage_s3: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_backup_remote_storage_s3** | [**CreateBackupRemoteStorageS3**](CreateBackupRemoteStorageS3.md)|  | 

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
**201** | Created |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_settings**
> create_settings(setting)

Create settings

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.setting import Setting
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
    api_instance = openapi_client.SettingsApi(api_client)
    setting = [openapi_client.Setting()] # List[Setting] | 

    try:
        # Create settings
        api_instance.create_settings(setting)
    except Exception as e:
        print("Exception when calling SettingsApi->create_settings: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **setting** | [**List[Setting]**](Setting.md)|  | 

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
**201** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_backup_remote_storage_s3**
> delete_backup_remote_storage_s3()

Delete S3 object storage settings at platform level.

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
    api_instance = openapi_client.SettingsApi(api_client)

    try:
        # Delete S3 object storage settings at platform level.
        api_instance.delete_backup_remote_storage_s3()
    except Exception as e:
        print("Exception when calling SettingsApi->delete_backup_remote_storage_s3: %s\n" % e)
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
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_global_service_setting**
> Outcome delete_global_service_setting(setting_kind, setting_key)

Delete a single global service setting

Delete a single global service setting value

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.outcome import Outcome
from openapi_client.models.setting_kind import SettingKind
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
    api_instance = openapi_client.SettingsApi(api_client)
    setting_kind = openapi_client.SettingKind() # SettingKind | The type of setting being applied
    setting_key = 'setting_key_example' # str | A key for updating an existing setting, some known values are - hard_delete_after_secs - letsencrypt_enabled - myhostname - org_websites_same_server - screenshot_driver_pool_size - screenshot_interval - sged_smtp - smtp_smart_host - website_backup

    try:
        # Delete a single global service setting
        api_response = api_instance.delete_global_service_setting(setting_kind, setting_key)
        print("The response of SettingsApi->delete_global_service_setting:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SettingsApi->delete_global_service_setting: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **setting_kind** | [**SettingKind**](.md)| The type of setting being applied | 
 **setting_key** | **str**| A key for updating an existing setting, some known values are - hard_delete_after_secs - letsencrypt_enabled - myhostname - org_websites_same_server - screenshot_driver_pool_size - screenshot_interval - sged_smtp - smtp_smart_host - website_backup | 

### Return type

[**Outcome**](Outcome.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**202** | Accepted but not applied |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_orchd_login_policy_email_blacklist**
> delete_orchd_login_policy_email_blacklist(orchd_login_policy_email_list)

Delete an orchd login policy email blacklist

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.orchd_login_policy_email_list import OrchdLoginPolicyEmailList
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
    api_instance = openapi_client.SettingsApi(api_client)
    orchd_login_policy_email_list = openapi_client.OrchdLoginPolicyEmailList() # OrchdLoginPolicyEmailList | 

    try:
        # Delete an orchd login policy email blacklist
        api_instance.delete_orchd_login_policy_email_blacklist(orchd_login_policy_email_list)
    except Exception as e:
        print("Exception when calling SettingsApi->delete_orchd_login_policy_email_blacklist: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orchd_login_policy_email_list** | [**OrchdLoginPolicyEmailList**](OrchdLoginPolicyEmailList.md)|  | 

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
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_orchd_login_policy_email_whitelist**
> delete_orchd_login_policy_email_whitelist(orchd_login_policy_email_list)

Delete an orchd login policy email whitelist

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.orchd_login_policy_email_list import OrchdLoginPolicyEmailList
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
    api_instance = openapi_client.SettingsApi(api_client)
    orchd_login_policy_email_list = openapi_client.OrchdLoginPolicyEmailList() # OrchdLoginPolicyEmailList | 

    try:
        # Delete an orchd login policy email whitelist
        api_instance.delete_orchd_login_policy_email_whitelist(orchd_login_policy_email_list)
    except Exception as e:
        print("Exception when calling SettingsApi->delete_orchd_login_policy_email_whitelist: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orchd_login_policy_email_list** | [**OrchdLoginPolicyEmailList**](OrchdLoginPolicyEmailList.md)|  | 

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
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_orchd_login_policy_ip_blacklist**
> delete_orchd_login_policy_ip_blacklist(orchd_login_policy_ip_list)

Delete an orchd login policy ip blacklist

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.orchd_login_policy_ip_list import OrchdLoginPolicyIpList
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
    api_instance = openapi_client.SettingsApi(api_client)
    orchd_login_policy_ip_list = openapi_client.OrchdLoginPolicyIpList() # OrchdLoginPolicyIpList | 

    try:
        # Delete an orchd login policy ip blacklist
        api_instance.delete_orchd_login_policy_ip_blacklist(orchd_login_policy_ip_list)
    except Exception as e:
        print("Exception when calling SettingsApi->delete_orchd_login_policy_ip_blacklist: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orchd_login_policy_ip_list** | [**OrchdLoginPolicyIpList**](OrchdLoginPolicyIpList.md)|  | 

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
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_orchd_login_policy_ip_whitelist**
> delete_orchd_login_policy_ip_whitelist(orchd_login_policy_ip_list)

Delete an orchd login policy ip whitelist

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.orchd_login_policy_ip_list import OrchdLoginPolicyIpList
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
    api_instance = openapi_client.SettingsApi(api_client)
    orchd_login_policy_ip_list = openapi_client.OrchdLoginPolicyIpList() # OrchdLoginPolicyIpList | 

    try:
        # Delete an orchd login policy ip whitelist
        api_instance.delete_orchd_login_policy_ip_whitelist(orchd_login_policy_ip_list)
    except Exception as e:
        print("Exception when calling SettingsApi->delete_orchd_login_policy_ip_whitelist: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orchd_login_policy_ip_list** | [**OrchdLoginPolicyIpList**](OrchdLoginPolicyIpList.md)|  | 

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
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_setting**
> delete_setting(name)

Remove the specified setting

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
    api_instance = openapi_client.SettingsApi(api_client)
    name = 'name_example' # str | The name of the resource.

    try:
        # Remove the specified setting
        api_instance.delete_setting(name)
    except Exception as e:
        print("Exception when calling SettingsApi->delete_setting: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **str**| The name of the resource. | 

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
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_backup_remote_storage_s3**
> BackupRemoteStorageS3 get_backup_remote_storage_s3()

Get S3 object storage settings at platform level.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.backup_remote_storage_s3 import BackupRemoteStorageS3
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
    api_instance = openapi_client.SettingsApi(api_client)

    try:
        # Get S3 object storage settings at platform level.
        api_response = api_instance.get_backup_remote_storage_s3()
        print("The response of SettingsApi->get_backup_remote_storage_s3:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SettingsApi->get_backup_remote_storage_s3: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**BackupRemoteStorageS3**](BackupRemoteStorageS3.md)

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

# **get_demo_mode**
> DemoMode get_demo_mode()

Get the demo mode status of the orchd service

### Example


```python
import openapi_client
from openapi_client.models.demo_mode import DemoMode
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
    api_instance = openapi_client.SettingsApi(api_client)

    try:
        # Get the demo mode status of the orchd service
        api_response = api_instance.get_demo_mode()
        print("The response of SettingsApi->get_demo_mode:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SettingsApi->get_demo_mode: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**DemoMode**](DemoMode.md)

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

# **get_docker_registry**
> DockerRegistry get_docker_registry()

Gets the Docker registry credentials.

Gets the Docker registry credentials.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.docker_registry import DockerRegistry
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
    api_instance = openapi_client.SettingsApi(api_client)

    try:
        # Gets the Docker registry credentials.
        api_response = api_instance.get_docker_registry()
        print("The response of SettingsApi->get_docker_registry:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SettingsApi->get_docker_registry: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**DockerRegistry**](DockerRegistry.md)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_global_service_setting**
> object get_global_service_setting(setting_kind)

Get the value for a particular global service setting

Returns the value for a particular global service setting as a JSON object

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.setting_kind import SettingKind
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
    api_instance = openapi_client.SettingsApi(api_client)
    setting_kind = openapi_client.SettingKind() # SettingKind | The type of setting being applied

    try:
        # Get the value for a particular global service setting
        api_response = api_instance.get_global_service_setting(setting_kind)
        print("The response of SettingsApi->get_global_service_setting:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SettingsApi->get_global_service_setting: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **setting_kind** | [**SettingKind**](.md)| The type of setting being applied | 

### Return type

**object**

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

# **get_orchd_log_settings**
> OrchdLogSettings get_orchd_log_settings()

Get the orchd log settings

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.orchd_log_settings import OrchdLogSettings
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
    api_instance = openapi_client.SettingsApi(api_client)

    try:
        # Get the orchd log settings
        api_response = api_instance.get_orchd_log_settings()
        print("The response of SettingsApi->get_orchd_log_settings:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SettingsApi->get_orchd_log_settings: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**OrchdLogSettings**](OrchdLogSettings.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_orchd_login_policy_email_blacklist**
> OrchdLoginPolicyEmailList get_orchd_login_policy_email_blacklist()

Get the orchd login policy email blacklist

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.orchd_login_policy_email_list import OrchdLoginPolicyEmailList
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
    api_instance = openapi_client.SettingsApi(api_client)

    try:
        # Get the orchd login policy email blacklist
        api_response = api_instance.get_orchd_login_policy_email_blacklist()
        print("The response of SettingsApi->get_orchd_login_policy_email_blacklist:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SettingsApi->get_orchd_login_policy_email_blacklist: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**OrchdLoginPolicyEmailList**](OrchdLoginPolicyEmailList.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_orchd_login_policy_email_whitelist**
> OrchdLoginPolicyEmailList get_orchd_login_policy_email_whitelist()

Get the orchd login policy email whitelist

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.orchd_login_policy_email_list import OrchdLoginPolicyEmailList
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
    api_instance = openapi_client.SettingsApi(api_client)

    try:
        # Get the orchd login policy email whitelist
        api_response = api_instance.get_orchd_login_policy_email_whitelist()
        print("The response of SettingsApi->get_orchd_login_policy_email_whitelist:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SettingsApi->get_orchd_login_policy_email_whitelist: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**OrchdLoginPolicyEmailList**](OrchdLoginPolicyEmailList.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_orchd_login_policy_ip_blacklist**
> OrchdLoginPolicyIpList get_orchd_login_policy_ip_blacklist()

Get the orchd login policy ip blacklist

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.orchd_login_policy_ip_list import OrchdLoginPolicyIpList
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
    api_instance = openapi_client.SettingsApi(api_client)

    try:
        # Get the orchd login policy ip blacklist
        api_response = api_instance.get_orchd_login_policy_ip_blacklist()
        print("The response of SettingsApi->get_orchd_login_policy_ip_blacklist:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SettingsApi->get_orchd_login_policy_ip_blacklist: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**OrchdLoginPolicyIpList**](OrchdLoginPolicyIpList.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_orchd_login_policy_ip_whitelist**
> OrchdLoginPolicyIpList get_orchd_login_policy_ip_whitelist()

Get the orchd login policy ip whitelist

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.orchd_login_policy_ip_list import OrchdLoginPolicyIpList
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
    api_instance = openapi_client.SettingsApi(api_client)

    try:
        # Get the orchd login policy ip whitelist
        api_response = api_instance.get_orchd_login_policy_ip_whitelist()
        print("The response of SettingsApi->get_orchd_login_policy_ip_whitelist:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SettingsApi->get_orchd_login_policy_ip_whitelist: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**OrchdLoginPolicyIpList**](OrchdLoginPolicyIpList.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_orchd_login_policy_settings**
> OrchdLoginPolicySettings get_orchd_login_policy_settings()

Get the orchd login policy settings

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.orchd_login_policy_settings import OrchdLoginPolicySettings
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
    api_instance = openapi_client.SettingsApi(api_client)

    try:
        # Get the orchd login policy settings
        api_response = api_instance.get_orchd_login_policy_settings()
        print("The response of SettingsApi->get_orchd_login_policy_settings:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SettingsApi->get_orchd_login_policy_settings: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**OrchdLoginPolicySettings**](OrchdLoginPolicySettings.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_prohibited_domains**
> str get_prohibited_domains()

Get the platform level prohibited domains as a newline separated list

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
    api_instance = openapi_client.SettingsApi(api_client)

    try:
        # Get the platform level prohibited domains as a newline separated list
        api_response = api_instance.get_prohibited_domains()
        print("The response of SettingsApi->get_prohibited_domains:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SettingsApi->get_prohibited_domains: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

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
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_setting**
> Setting get_setting(name)

Get the specified setting

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.setting import Setting
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
    api_instance = openapi_client.SettingsApi(api_client)
    name = 'name_example' # str | The name of the resource.

    try:
        # Get the specified setting
        api_response = api_instance.get_setting(name)
        print("The response of SettingsApi->get_setting:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SettingsApi->get_setting: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **str**| The name of the resource. | 

### Return type

[**Setting**](Setting.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_settings**
> SettingsFullListing get_settings()

Get all current settings

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.settings_full_listing import SettingsFullListing
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
    api_instance = openapi_client.SettingsApi(api_client)

    try:
        # Get all current settings
        api_response = api_instance.get_settings()
        print("The response of SettingsApi->get_settings:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SettingsApi->get_settings: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**SettingsFullListing**](SettingsFullListing.md)

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

# **set_docker_registry**
> set_docker_registry(docker_registry=docker_registry)

Updates the Docker registry credentials.

Sets the Docker registry credentials, overwriting any previous one if one exists.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.docker_registry import DockerRegistry
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
    api_instance = openapi_client.SettingsApi(api_client)
    docker_registry = openapi_client.DockerRegistry() # DockerRegistry |  (optional)

    try:
        # Updates the Docker registry credentials.
        api_instance.set_docker_registry(docker_registry=docker_registry)
    except Exception as e:
        print("Exception when calling SettingsApi->set_docker_registry: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **docker_registry** | [**DockerRegistry**](DockerRegistry.md)|  | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_global_service_setting**
> Outcome set_global_service_setting(setting_kind, setting_key, service_setting_value)

Set a single global service setting

Set or replace a single global service setting

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.outcome import Outcome
from openapi_client.models.service_setting_value import ServiceSettingValue
from openapi_client.models.setting_kind import SettingKind
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
    api_instance = openapi_client.SettingsApi(api_client)
    setting_kind = openapi_client.SettingKind() # SettingKind | The type of setting being applied
    setting_key = 'setting_key_example' # str | A key for updating an existing setting, some known values are - hard_delete_after_secs - letsencrypt_enabled - myhostname - org_websites_same_server - screenshot_driver_pool_size - screenshot_interval - sged_smtp - smtp_smart_host - website_backup
    service_setting_value = openapi_client.ServiceSettingValue() # ServiceSettingValue | 

    try:
        # Set a single global service setting
        api_response = api_instance.set_global_service_setting(setting_kind, setting_key, service_setting_value)
        print("The response of SettingsApi->set_global_service_setting:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SettingsApi->set_global_service_setting: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **setting_kind** | [**SettingKind**](.md)| The type of setting being applied | 
 **setting_key** | **str**| A key for updating an existing setting, some known values are - hard_delete_after_secs - letsencrypt_enabled - myhostname - org_websites_same_server - screenshot_driver_pool_size - screenshot_interval - sged_smtp - smtp_smart_host - website_backup | 
 **service_setting_value** | [**ServiceSettingValue**](ServiceSettingValue.md)|  | 

### Return type

[**Outcome**](Outcome.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**202** | Accepted but not applied |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_orchd_log_settings**
> set_orchd_log_settings(orchd_log_settings)

Set the orchd log settings

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.orchd_log_settings import OrchdLogSettings
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
    api_instance = openapi_client.SettingsApi(api_client)
    orchd_log_settings = openapi_client.OrchdLogSettings() # OrchdLogSettings | 

    try:
        # Set the orchd log settings
        api_instance.set_orchd_log_settings(orchd_log_settings)
    except Exception as e:
        print("Exception when calling SettingsApi->set_orchd_log_settings: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orchd_log_settings** | [**OrchdLogSettings**](OrchdLogSettings.md)|  | 

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
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_prohibited_domains**
> set_prohibited_domains(body)

Set the platform level prohibited domains

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
    api_instance = openapi_client.SettingsApi(api_client)
    body = 'body_example' # str | 

    try:
        # Set the platform level prohibited domains
        api_instance.set_prohibited_domains(body)
    except Exception as e:
        print("Exception when calling SettingsApi->set_prohibited_domains: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **str**|  | 

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
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_backup_remote_storage_s3**
> update_backup_remote_storage_s3(update_backup_remote_storage_s3)

Update S3 object storage settings at platform level.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.update_backup_remote_storage_s3 import UpdateBackupRemoteStorageS3
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
    api_instance = openapi_client.SettingsApi(api_client)
    update_backup_remote_storage_s3 = openapi_client.UpdateBackupRemoteStorageS3() # UpdateBackupRemoteStorageS3 | 

    try:
        # Update S3 object storage settings at platform level.
        api_instance.update_backup_remote_storage_s3(update_backup_remote_storage_s3)
    except Exception as e:
        print("Exception when calling SettingsApi->update_backup_remote_storage_s3: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **update_backup_remote_storage_s3** | [**UpdateBackupRemoteStorageS3**](UpdateBackupRemoteStorageS3.md)|  | 

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

# **update_setting**
> update_setting(name, update_setting_request)

Create or update the specified setting

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.update_setting_request import UpdateSettingRequest
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
    api_instance = openapi_client.SettingsApi(api_client)
    name = 'name_example' # str | The name of the resource.
    update_setting_request = openapi_client.UpdateSettingRequest() # UpdateSettingRequest | 

    try:
        # Create or update the specified setting
        api_instance.update_setting(name, update_setting_request)
    except Exception as e:
        print("Exception when calling SettingsApi->update_setting: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **str**| The name of the resource. | 
 **update_setting_request** | [**UpdateSettingRequest**](UpdateSettingRequest.md)|  | 

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
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

