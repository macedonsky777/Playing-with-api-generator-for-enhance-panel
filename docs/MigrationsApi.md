# openapi_client.MigrationsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_migration**](MigrationsApi.md#create_migration) | **POST** /migrations | Create website role migration
[**create_migration_session**](MigrationsApi.md#create_migration_session) | **POST** /migrations/sessions | Create bulk website role migrations
[**get_migration**](MigrationsApi.md#get_migration) | **GET** /migrations/{migrationId} | Get a single migration
[**get_migration_log**](MigrationsApi.md#get_migration_log) | **GET** /migrations/{migrationId}/log | Get the log for a migration
[**get_migration_sessions**](MigrationsApi.md#get_migration_sessions) | **GET** /migrations/sessions | Get website role migration sessions
[**get_migrations**](MigrationsApi.md#get_migrations) | **GET** /migrations | Get website role migrations


# **create_migration**
> NewResourceUuid create_migration(new_migration_details)

Create website role migration

Create a new role website migration from one server to another. Deprecated in favor of createMigrationSession.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.new_migration_details import NewMigrationDetails
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
    api_instance = openapi_client.MigrationsApi(api_client)
    new_migration_details = openapi_client.NewMigrationDetails() # NewMigrationDetails | Migration details.

    try:
        # Create website role migration
        api_response = api_instance.create_migration(new_migration_details)
        print("The response of MigrationsApi->create_migration:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MigrationsApi->create_migration: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **new_migration_details** | [**NewMigrationDetails**](NewMigrationDetails.md)| Migration details. | 

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
**201** | Migration created |  -  |
**400** | Invalid parameters |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_migration_session**
> MigrationSessionCreationOk create_migration_session(new_migration_details)

Create bulk website role migrations

Create many new role website migration from one server to another. The migrations are grouped with a session id. If any migration fails to schedule, 206 is returned. If all migrations fail to schedule, 400 is returned. See the body for error messages in both cases.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.migration_session_creation_ok import MigrationSessionCreationOk
from openapi_client.models.new_migration_details import NewMigrationDetails
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
    api_instance = openapi_client.MigrationsApi(api_client)
    new_migration_details = [openapi_client.NewMigrationDetails()] # List[NewMigrationDetails] | Migrations details.

    try:
        # Create bulk website role migrations
        api_response = api_instance.create_migration_session(new_migration_details)
        print("The response of MigrationsApi->create_migration_session:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MigrationsApi->create_migration_session: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **new_migration_details** | [**List[NewMigrationDetails]**](NewMigrationDetails.md)| Migrations details. | 

### Return type

[**MigrationSessionCreationOk**](MigrationSessionCreationOk.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | All migrations created |  -  |
**206** | Some migrations failed to create, see body for details |  -  |
**400** | All migrations failed to create, see body for details |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_migration**
> MigrationDetails get_migration(migration_id)

Get a single migration

Fetches the details of a single server migration.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.migration_details import MigrationDetails
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
    api_instance = openapi_client.MigrationsApi(api_client)
    migration_id = 'migration_id_example' # str | The ID of the migration being acted upon.

    try:
        # Get a single migration
        api_response = api_instance.get_migration(migration_id)
        print("The response of MigrationsApi->get_migration:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MigrationsApi->get_migration: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **migration_id** | **str**| The ID of the migration being acted upon. | 

### Return type

[**MigrationDetails**](MigrationDetails.md)

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

# **get_migration_log**
> List[MigrationLog] get_migration_log(migration_id)

Get the log for a migration

Fetches the migration log for a single server migration.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.migration_log import MigrationLog
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
    api_instance = openapi_client.MigrationsApi(api_client)
    migration_id = 'migration_id_example' # str | The ID of the migration being acted upon.

    try:
        # Get the log for a migration
        api_response = api_instance.get_migration_log(migration_id)
        print("The response of MigrationsApi->get_migration_log:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MigrationsApi->get_migration_log: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **migration_id** | **str**| The ID of the migration being acted upon. | 

### Return type

[**List[MigrationLog]**](MigrationLog.md)

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

# **get_migration_sessions**
> MigrationSessionsListing get_migration_sessions(offset=offset, limit=limit, sort_order=sort_order, sort_by=sort_by, created_by=created_by, search_domain=search_domain)

Get website role migration sessions

Migration sessions group server migrations together under one id. This endpoint lists sessions, when were they created and when was any migration in the session last updated. If searching by domain, the resulting migrationCount is the number of migrations in the session that match the search criteria. If searching with createdBy, you can search by the email of the user who created the session. If the session was created with an API key, createdBy will be set to \"via API\". Legacy migrations created with deprecated \"createMigration\" endpoint are assigned under session that has createdBy set to \"legacy migrations\"

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.migration_sessions_listing import MigrationSessionsListing
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
    api_instance = openapi_client.MigrationsApi(api_client)
    offset = 56 # int | The offset from which to return items. (optional)
    limit = 56 # int | The maximum number of items to return. (optional)
    sort_order = 'sort_order_example' # str | The direction in which to sort. Possible values are 'asc' and 'desc', defaulting to 'asc'. (optional)
    sort_by = 'sort_by_example' # str | The field by which to sort. (optional)
    created_by = 'created_by_example' # str | Look for a specific session creator in the result set. (optional)
    search_domain = 'search_domain_example' # str | Look for a specific domain in the result set. (optional)

    try:
        # Get website role migration sessions
        api_response = api_instance.get_migration_sessions(offset=offset, limit=limit, sort_order=sort_order, sort_by=sort_by, created_by=created_by, search_domain=search_domain)
        print("The response of MigrationsApi->get_migration_sessions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MigrationsApi->get_migration_sessions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **offset** | **int**| The offset from which to return items. | [optional] 
 **limit** | **int**| The maximum number of items to return. | [optional] 
 **sort_order** | **str**| The direction in which to sort. Possible values are &#39;asc&#39; and &#39;desc&#39;, defaulting to &#39;asc&#39;. | [optional] 
 **sort_by** | **str**| The field by which to sort. | [optional] 
 **created_by** | **str**| Look for a specific session creator in the result set. | [optional] 
 **search_domain** | **str**| Look for a specific domain in the result set. | [optional] 

### Return type

[**MigrationSessionsListing**](MigrationSessionsListing.md)

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

# **get_migrations**
> MigrationsListing get_migrations(offset=offset, limit=limit, sort_order=sort_order, sort_by=sort_by, search_domain=search_domain, migration_status=migration_status, session_id=session_id)

Get website role migrations

Lists all server migrations, whether pending, in progress, failed or completed.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.migration_status import MigrationStatus
from openapi_client.models.migrations_listing import MigrationsListing
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
    api_instance = openapi_client.MigrationsApi(api_client)
    offset = 56 # int | The offset from which to return items. (optional)
    limit = 56 # int | The maximum number of items to return. (optional)
    sort_order = 'sort_order_example' # str | The direction in which to sort. Possible values are 'asc' and 'desc', defaulting to 'asc'. (optional)
    sort_by = 'sort_by_example' # str | The field by which to sort. (optional)
    search_domain = 'search_domain_example' # str | Look for a specific domain in the result set. (optional)
    migration_status = openapi_client.MigrationStatus() # MigrationStatus | Filter by a particular migration status (optional)
    session_id = 'session_id_example' # str | Filter for a specific migration session. (optional)

    try:
        # Get website role migrations
        api_response = api_instance.get_migrations(offset=offset, limit=limit, sort_order=sort_order, sort_by=sort_by, search_domain=search_domain, migration_status=migration_status, session_id=session_id)
        print("The response of MigrationsApi->get_migrations:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MigrationsApi->get_migrations: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **offset** | **int**| The offset from which to return items. | [optional] 
 **limit** | **int**| The maximum number of items to return. | [optional] 
 **sort_order** | **str**| The direction in which to sort. Possible values are &#39;asc&#39; and &#39;desc&#39;, defaulting to &#39;asc&#39;. | [optional] 
 **sort_by** | **str**| The field by which to sort. | [optional] 
 **search_domain** | **str**| Look for a specific domain in the result set. | [optional] 
 **migration_status** | [**MigrationStatus**](.md)| Filter by a particular migration status | [optional] 
 **session_id** | **str**| Filter for a specific migration session. | [optional] 

### Return type

[**MigrationsListing**](MigrationsListing.md)

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

