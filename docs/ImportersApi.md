# openapi_client.ImportersApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**analyze_import_migration**](ImportersApi.md#analyze_import_migration) | **POST** /v2/orgs/{org_id}/import/{import_migration_id}/analyze | Analyze imported migration
[**check_import_migration_resources**](ImportersApi.md#check_import_migration_resources) | **POST** /v2/orgs/{org_id}/import/{import_migration_id}/resource | Check if all resources from the imported migration could be created.
[**create_import_migration**](ImportersApi.md#create_import_migration) | **POST** /v2/orgs/{org_id}/import/{import_migration_id} | Create a new import migration.
[**create_import_server_settings**](ImportersApi.md#create_import_server_settings) | **POST** /orgs/{org_id}/import/server/settings | Create settings for the server import
[**delete_import_migration**](ImportersApi.md#delete_import_migration) | **DELETE** /v2/orgs/{org_id}/import/{import_migration_id} | Delete single migration
[**delete_import_server_settings**](ImportersApi.md#delete_import_server_settings) | **DELETE** /orgs/{org_id}/import/server/{server_id}/settings | Delete settings for the server import
[**get_import_migration**](ImportersApi.md#get_import_migration) | **GET** /v2/orgs/{org_id}/import/{import_migration_id} | Fetches single migration details
[**get_import_migration_data**](ImportersApi.md#get_import_migration_data) | **GET** /v2/orgs/{org_id}/import/{import_migration_id}/analyze | Get import migration information
[**get_import_migration_log**](ImportersApi.md#get_import_migration_log) | **GET** /v2/orgs/{org_id}/import/{import_migration_id}/log | Get the log for an import migration
[**get_import_migrations**](ImportersApi.md#get_import_migrations) | **GET** /v2/orgs/{org_id}/import | List all import migrations
[**get_import_server_domains_cached**](ImportersApi.md#get_import_server_domains_cached) | **GET** /orgs/{org_id}/import/server/{server_id}/cached-domains | Returns cached domains
[**get_import_server_pull_domains**](ImportersApi.md#get_import_server_pull_domains) | **GET** /orgs/{org_id}/import/server/{server_id}/pull-domains | Pull domains form the remote server.
[**get_import_server_settings**](ImportersApi.md#get_import_server_settings) | **GET** /orgs/{org_id}/import/server/{server_id}/settings | Get settings for the server import
[**list_import_server_settings**](ImportersApi.md#list_import_server_settings) | **GET** /orgs/{org_id}/import/server/settings | List all server import settings
[**scan_import_migrations**](ImportersApi.md#scan_import_migrations) | **GET** /v2/import/scan | Scan for manually uploaded cPanel backups.
[**transfer_c_panel_user_account**](ImportersApi.md#transfer_c_panel_user_account) | **POST** /orgs/{org_id}/import/server/{server_id}/account/{user_id} | Transfer user account from remote cPanel server
[**update_import_server_settings**](ImportersApi.md#update_import_server_settings) | **PATCH** /orgs/{org_id}/import/server/{server_id}/settings | Update settings for the server import
[**upload_import_migration**](ImportersApi.md#upload_import_migration) | **POST** /v2/orgs/{org_id}/import/upload/{import_migration_kind} | Upload file for analyzing and processing.


# **analyze_import_migration**
> analyze_import_migration(org_id, import_migration_id)

Analyze imported migration

Analyze import and store results into database.  Note: the endpoint returns immediately, and you have to poll status via `getImportMigration` endpoint. If you want to see detailed error, please call `getImportMigrationLog`. 

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
    api_instance = openapi_client.ImportersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    import_migration_id = 'import_migration_id_example' # str | The ID of the import migration being acted upon.

    try:
        # Analyze imported migration
        api_instance.analyze_import_migration(org_id, import_migration_id)
    except Exception as e:
        print("Exception when calling ImportersApi->analyze_import_migration: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **import_migration_id** | **str**| The ID of the import migration being acted upon. | 

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
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **check_import_migration_resources**
> ResourceCheckError check_import_migration_resources(org_id, import_migration_id, importer_migration_req_body=importer_migration_req_body)

Check if all resources from the imported migration could be created.

Check if all resources from the imported migration could be created.  If all resources could be created, 200 is returned with an empty `ResourceCheckError`. However, if any error occurs, 200 is returned with a non-empty `ResourceCheckError`.  In case of import failure, you can rerun importing by setting forceQueue to true. Before doing so, it's required to remove any already imported resources. Otherwise, the import will fail. 

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.importer_migration_req_body import ImporterMigrationReqBody
from openapi_client.models.resource_check_error import ResourceCheckError
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
    api_instance = openapi_client.ImportersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    import_migration_id = 'import_migration_id_example' # str | The ID of the import migration being acted upon.
    importer_migration_req_body = openapi_client.ImporterMigrationReqBody() # ImporterMigrationReqBody |  (optional)

    try:
        # Check if all resources from the imported migration could be created.
        api_response = api_instance.check_import_migration_resources(org_id, import_migration_id, importer_migration_req_body=importer_migration_req_body)
        print("The response of ImportersApi->check_import_migration_resources:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ImportersApi->check_import_migration_resources: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **import_migration_id** | **str**| The ID of the import migration being acted upon. | 
 **importer_migration_req_body** | [**ImporterMigrationReqBody**](ImporterMigrationReqBody.md)|  | [optional] 

### Return type

[**ResourceCheckError**](ResourceCheckError.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_import_migration**
> create_import_migration(org_id, import_migration_id, importer_migration_req_body=importer_migration_req_body)

Create a new import migration.

Create a new import migration for a given import type.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.importer_migration_req_body import ImporterMigrationReqBody
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
    api_instance = openapi_client.ImportersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    import_migration_id = 'import_migration_id_example' # str | The ID of the import migration being acted upon.
    importer_migration_req_body = openapi_client.ImporterMigrationReqBody() # ImporterMigrationReqBody |  (optional)

    try:
        # Create a new import migration.
        api_instance.create_import_migration(org_id, import_migration_id, importer_migration_req_body=importer_migration_req_body)
    except Exception as e:
        print("Exception when calling ImportersApi->create_import_migration: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **import_migration_id** | **str**| The ID of the import migration being acted upon. | 
 **importer_migration_req_body** | [**ImporterMigrationReqBody**](ImporterMigrationReqBody.md)|  | [optional] 

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
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_import_server_settings**
> NewResourceUuid create_import_server_settings(org_id, new_import_server_settings)

Create settings for the server import

Create settings for the server import.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_import_server_settings import NewImportServerSettings
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
    api_instance = openapi_client.ImportersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    new_import_server_settings = openapi_client.NewImportServerSettings() # NewImportServerSettings | 

    try:
        # Create settings for the server import
        api_response = api_instance.create_import_server_settings(org_id, new_import_server_settings)
        print("The response of ImportersApi->create_import_server_settings:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ImportersApi->create_import_server_settings: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **new_import_server_settings** | [**NewImportServerSettings**](NewImportServerSettings.md)|  | 

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
**201** | Created |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_import_migration**
> delete_import_migration(org_id, import_migration_id)

Delete single migration

Delete a single migration with the uploaded file.

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
    api_instance = openapi_client.ImportersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    import_migration_id = 'import_migration_id_example' # str | The ID of the import migration being acted upon.

    try:
        # Delete single migration
        api_instance.delete_import_migration(org_id, import_migration_id)
    except Exception as e:
        print("Exception when calling ImportersApi->delete_import_migration: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **import_migration_id** | **str**| The ID of the import migration being acted upon. | 

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
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_import_server_settings**
> delete_import_server_settings(org_id, server_id)

Delete settings for the server import

Delete settings for the server import.

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
    api_instance = openapi_client.ImportersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Delete settings for the server import
        api_instance.delete_import_server_settings(org_id, server_id)
    except Exception as e:
        print("Exception when calling ImportersApi->delete_import_server_settings: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **server_id** | **str**| The UUID of the server | 

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
**200** | Query successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_import_migration**
> ImportMigrationEntry get_import_migration(org_id, import_migration_id)

Fetches single migration details

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.import_migration_entry import ImportMigrationEntry
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
    api_instance = openapi_client.ImportersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    import_migration_id = 'import_migration_id_example' # str | The ID of the import migration being acted upon.

    try:
        # Fetches single migration details
        api_response = api_instance.get_import_migration(org_id, import_migration_id)
        print("The response of ImportersApi->get_import_migration:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ImportersApi->get_import_migration: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **import_migration_id** | **str**| The ID of the import migration being acted upon. | 

### Return type

[**ImportMigrationEntry**](ImportMigrationEntry.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Query successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_import_migration_data**
> ImporterAnalyzedData get_import_migration_data(org_id, import_migration_id)

Get import migration information

Get analyzed informations about import.  Information contains details about domains, ftp users, databases, crontabs and mailboxes. 

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.importer_analyzed_data import ImporterAnalyzedData
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
    api_instance = openapi_client.ImportersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    import_migration_id = 'import_migration_id_example' # str | The ID of the import migration being acted upon.

    try:
        # Get import migration information
        api_response = api_instance.get_import_migration_data(org_id, import_migration_id)
        print("The response of ImportersApi->get_import_migration_data:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ImportersApi->get_import_migration_data: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **import_migration_id** | **str**| The ID of the import migration being acted upon. | 

### Return type

[**ImporterAnalyzedData**](ImporterAnalyzedData.md)

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

# **get_import_migration_log**
> List[ImportMigrationLogEntry] get_import_migration_log(org_id, import_migration_id)

Get the log for an import migration

Fetches the import migration log for a single import migration.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.import_migration_log_entry import ImportMigrationLogEntry
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
    api_instance = openapi_client.ImportersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    import_migration_id = 'import_migration_id_example' # str | The ID of the import migration being acted upon.

    try:
        # Get the log for an import migration
        api_response = api_instance.get_import_migration_log(org_id, import_migration_id)
        print("The response of ImportersApi->get_import_migration_log:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ImportersApi->get_import_migration_log: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **import_migration_id** | **str**| The ID of the import migration being acted upon. | 

### Return type

[**List[ImportMigrationLogEntry]**](ImportMigrationLogEntry.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Query successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_import_migrations**
> ImportMigrationFullListing get_import_migrations(org_id)

List all import migrations

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.import_migration_full_listing import ImportMigrationFullListing
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
    api_instance = openapi_client.ImportersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.

    try:
        # List all import migrations
        api_response = api_instance.get_import_migrations(org_id)
        print("The response of ImportersApi->get_import_migrations:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ImportersApi->get_import_migrations: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 

### Return type

[**ImportMigrationFullListing**](ImportMigrationFullListing.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Query successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_import_server_domains_cached**
> ImportServerDomainsListing get_import_server_domains_cached(org_id, server_id, offset=offset, limit=limit, sort_order=sort_order, search_domain=search_domain, sort_by=sort_by)

Returns cached domains

Returns cached domains.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.import_server_domains_listing import ImportServerDomainsListing
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
    api_instance = openapi_client.ImportersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    server_id = 'server_id_example' # str | The UUID of the server
    offset = 56 # int | The offset from which to return items. (optional)
    limit = 56 # int | The maximum number of items to return. (optional)
    sort_order = 'sort_order_example' # str | The direction in which to sort. Possible values are 'asc' and 'desc', defaulting to 'asc'. (optional)
    search_domain = 'search_domain_example' # str | Look for a specific domain in the result set. (optional)
    sort_by = 'sort_by_example' # str | The field by which to sort. (optional)

    try:
        # Returns cached domains
        api_response = api_instance.get_import_server_domains_cached(org_id, server_id, offset=offset, limit=limit, sort_order=sort_order, search_domain=search_domain, sort_by=sort_by)
        print("The response of ImportersApi->get_import_server_domains_cached:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ImportersApi->get_import_server_domains_cached: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **server_id** | **str**| The UUID of the server | 
 **offset** | **int**| The offset from which to return items. | [optional] 
 **limit** | **int**| The maximum number of items to return. | [optional] 
 **sort_order** | **str**| The direction in which to sort. Possible values are &#39;asc&#39; and &#39;desc&#39;, defaulting to &#39;asc&#39;. | [optional] 
 **search_domain** | **str**| Look for a specific domain in the result set. | [optional] 
 **sort_by** | **str**| The field by which to sort. | [optional] 

### Return type

[**ImportServerDomainsListing**](ImportServerDomainsListing.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Query successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_import_server_pull_domains**
> ImportServerDomainsFullListing get_import_server_pull_domains(org_id, server_id)

Pull domains form the remote server.

Pull domains form the remote server, and cache them. To get cached domains, use getImportServerDomainsCached.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.import_server_domains_full_listing import ImportServerDomainsFullListing
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
    api_instance = openapi_client.ImportersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Pull domains form the remote server.
        api_response = api_instance.get_import_server_pull_domains(org_id, server_id)
        print("The response of ImportersApi->get_import_server_pull_domains:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ImportersApi->get_import_server_pull_domains: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **server_id** | **str**| The UUID of the server | 

### Return type

[**ImportServerDomainsFullListing**](ImportServerDomainsFullListing.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Query successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_import_server_settings**
> ImportServerSettings get_import_server_settings(org_id, server_id)

Get settings for the server import

Get settings for the server import. Note: returned data does not contain ssh private key or any passwords/tokens.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.import_server_settings import ImportServerSettings
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
    api_instance = openapi_client.ImportersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    server_id = 'server_id_example' # str | The UUID of the server

    try:
        # Get settings for the server import
        api_response = api_instance.get_import_server_settings(org_id, server_id)
        print("The response of ImportersApi->get_import_server_settings:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ImportersApi->get_import_server_settings: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **server_id** | **str**| The UUID of the server | 

### Return type

[**ImportServerSettings**](ImportServerSettings.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Query successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_import_server_settings**
> ImportServerSettingsFullListing list_import_server_settings(org_id)

List all server import settings

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.import_server_settings_full_listing import ImportServerSettingsFullListing
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
    api_instance = openapi_client.ImportersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.

    try:
        # List all server import settings
        api_response = api_instance.list_import_server_settings(org_id)
        print("The response of ImportersApi->list_import_server_settings:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ImportersApi->list_import_server_settings: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 

### Return type

[**ImportServerSettingsFullListing**](ImportServerSettingsFullListing.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **scan_import_migrations**
> List[str] scan_import_migrations()

Scan for manually uploaded cPanel backups.

Will scan /var/local/enhance/orchd/importer for files matching cpmove*.tar.gz or backup*.tar.gz and will add them to the importer database for analysis.  An array of migration IDs will be returned. Master organisation only. 

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
    api_instance = openapi_client.ImportersApi(api_client)

    try:
        # Scan for manually uploaded cPanel backups.
        api_response = api_instance.scan_import_migrations()
        print("The response of ImportersApi->scan_import_migrations:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ImportersApi->scan_import_migrations: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

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
**201** | Migrations found |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **transfer_c_panel_user_account**
> NewResourceUuid transfer_c_panel_user_account(org_id, server_id, user_id, transfer_user_account_req_body=transfer_user_account_req_body)

Transfer user account from remote cPanel server

Transfer user account from remote cPanel server to Enhance server. It's an async endpoint. To get transfer result, you have to call getImportMigration.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_resource_uuid import NewResourceUuid
from openapi_client.models.transfer_user_account_req_body import TransferUserAccountReqBody
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
    api_instance = openapi_client.ImportersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    server_id = 'server_id_example' # str | The UUID of the server
    user_id = 'user_id_example' # str | The ID of the remote cPanel user
    transfer_user_account_req_body = openapi_client.TransferUserAccountReqBody() # TransferUserAccountReqBody |  (optional)

    try:
        # Transfer user account from remote cPanel server
        api_response = api_instance.transfer_c_panel_user_account(org_id, server_id, user_id, transfer_user_account_req_body=transfer_user_account_req_body)
        print("The response of ImportersApi->transfer_c_panel_user_account:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ImportersApi->transfer_c_panel_user_account: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **server_id** | **str**| The UUID of the server | 
 **user_id** | **str**| The ID of the remote cPanel user | 
 **transfer_user_account_req_body** | [**TransferUserAccountReqBody**](TransferUserAccountReqBody.md)|  | [optional] 

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
**201** | Upload created |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_import_server_settings**
> update_import_server_settings(org_id, server_id, update_import_server_settings)

Update settings for the server import

Update settings for the server import.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.update_import_server_settings import UpdateImportServerSettings
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
    api_instance = openapi_client.ImportersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    server_id = 'server_id_example' # str | The UUID of the server
    update_import_server_settings = openapi_client.UpdateImportServerSettings() # UpdateImportServerSettings | 

    try:
        # Update settings for the server import
        api_instance.update_import_server_settings(org_id, server_id, update_import_server_settings)
    except Exception as e:
        print("Exception when calling ImportersApi->update_import_server_settings: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **server_id** | **str**| The UUID of the server | 
 **update_import_server_settings** | [**UpdateImportServerSettings**](UpdateImportServerSettings.md)|  | 

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
**200** | Query successful |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upload_import_migration**
> NewResourceUuid upload_import_migration(org_id, import_migration_kind, backup=backup)

Upload file for analyzing and processing.

Uploads an import file. File must be in `tar.gz` format, and only cPanel and Plesk uploads are allowed.  The max allowed size is 100 GB. 

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
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
    api_instance = openapi_client.ImportersApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    import_migration_kind = 'import_migration_kind_example' # str | The type of migration file being uploaded.
    backup = None # bytearray |  (optional)

    try:
        # Upload file for analyzing and processing.
        api_response = api_instance.upload_import_migration(org_id, import_migration_kind, backup=backup)
        print("The response of ImportersApi->upload_import_migration:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ImportersApi->upload_import_migration: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **import_migration_kind** | **str**| The type of migration file being uploaded. | 
 **backup** | **bytearray**|  | [optional] 

### Return type

[**NewResourceUuid**](NewResourceUuid.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Upload created |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

