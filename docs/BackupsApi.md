# openapi_client.BackupsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**backup_website**](BackupsApi.md#backup_website) | **POST** /orgs/{org_id}/websites/{website_id}/backups | Create a website backup
[**delete_website_backup**](BackupsApi.md#delete_website_backup) | **DELETE** /orgs/{org_id}/websites/{website_id}/backups/{backup_id} | Delete a backup
[**get_website_backup**](BackupsApi.md#get_website_backup) | **GET** /orgs/{org_id}/websites/{website_id}/backups/{backup_id} | Get detailed metadata of the website backup
[**get_website_backups**](BackupsApi.md#get_website_backups) | **GET** /orgs/{org_id}/websites/{website_id}/backups | Get all website backups metadata
[**get_website_restore_status**](BackupsApi.md#get_website_restore_status) | **GET** /orgs/{org_id}/websites/{website_id}/backups/{backup_id}/restore_status | Get the last detailed metadata of the restored website backup.
[**restore_website**](BackupsApi.md#restore_website) | **PUT** /orgs/{org_id}/websites/{website_id}/backups/{backup_id} | Restore website from a backup


# **backup_website**
> Backup backup_website(org_id, website_id, include_emails=include_emails, backup_options=backup_options)

Create a website backup

Creates a new full website backup. This is a long running operation and the request doesn't return until all backups are finished, or an error occurs. If you want to see the backup progress, you can periodically query the backup status via `getWebsiteBackupStatus`. Backups consists of several components, and a component is the smallest granularity of a backup. The components are: backing up of the website's home directory, the website's mysql databases, and the website's emails. The backups may be partial, that is, some out of all backup components may succeeded, but e.g. the backup of the mysql databases may fail. In both cases, the backup snapshot is still created, and the mysql backups are marked as failed for the backup record. Email backups are not done automatically, as they need not be backed up in most cases (due to the expectation that customers would want to backup and then roll back a website after filesystem or database changes, which wouldn't concern emails). Doing so redundantly is time consuming so it is skipped by default, but emails may be backed up if the `includeEmails` query parameter is set to true. If the backup fails altogether, this endpoint still returns a 201 Created, but in this case only the metadata in `orchd`'s db is inserted, no actual backup snapshot is created. This is for information purposes, such a backup, perhaps needless to say, cannot be restored. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.backup import Backup
from openapi_client.models.backup_options import BackupOptions
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
    api_instance = openapi_client.BackupsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    include_emails = False # bool | The boolean flag used to include emails in the backup. (optional) (default to False)
    backup_options = openapi_client.BackupOptions() # BackupOptions |  (optional)

    try:
        # Create a website backup
        api_response = api_instance.backup_website(org_id, website_id, include_emails=include_emails, backup_options=backup_options)
        print("The response of BackupsApi->backup_website:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BackupsApi->backup_website: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **include_emails** | **bool**| The boolean flag used to include emails in the backup. | [optional] [default to False]
 **backup_options** | [**BackupOptions**](BackupOptions.md)|  | [optional] 

### Return type

[**Backup**](Backup.md)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

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

# **delete_website_backup**
> delete_website_backup(org_id, website_id, backup_id)

Delete a backup

Deletes a backup. If the backup refers to a (partially) successful backup, both its metadata and the backup snapshot on the backup server will be removed, otherwise just the metadata is removed. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

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
    api_instance = openapi_client.BackupsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    backup_id = 56 # int | The id of the backup.

    try:
        # Delete a backup
        api_instance.delete_website_backup(org_id, website_id, backup_id)
    except Exception as e:
        print("Exception when calling BackupsApi->delete_website_backup: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **backup_id** | **int**| The id of the backup. | 

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
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_backup**
> BackupDetailed get_website_backup(org_id, website_id, backup_id)

Get detailed metadata of the website backup

Returns detailed information about the backup. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.backup_detailed import BackupDetailed
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
    api_instance = openapi_client.BackupsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    backup_id = 56 # int | The id of the backup.

    try:
        # Get detailed metadata of the website backup
        api_response = api_instance.get_website_backup(org_id, website_id, backup_id)
        print("The response of BackupsApi->get_website_backup:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BackupsApi->get_website_backup: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **backup_id** | **int**| The id of the backup. | 

### Return type

[**BackupDetailed**](BackupDetailed.md)

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
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_backups**
> BackupsFullListing get_website_backups(org_id, website_id)

Get all website backups metadata

Returns a list of all website backups. This includes the backups that were not successful as well, or backups that were only partially successful (e.g. the home directory was backed up but not the databases). Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.backups_full_listing import BackupsFullListing
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
    api_instance = openapi_client.BackupsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Get all website backups metadata
        api_response = api_instance.get_website_backups(org_id, website_id)
        print("The response of BackupsApi->get_website_backups:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BackupsApi->get_website_backups: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 

### Return type

[**BackupsFullListing**](BackupsFullListing.md)

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
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_restore_status**
> RestoreDetailed get_website_restore_status(org_id, website_id, backup_id)

Get the last detailed metadata of the restored website backup.

Returns the last detailed information about the restored backup. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.restore_detailed import RestoreDetailed
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
    api_instance = openapi_client.BackupsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    backup_id = 56 # int | The id of the backup.

    try:
        # Get the last detailed metadata of the restored website backup.
        api_response = api_instance.get_website_restore_status(org_id, website_id, backup_id)
        print("The response of BackupsApi->get_website_restore_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BackupsApi->get_website_restore_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **backup_id** | **int**| The id of the backup. | 

### Return type

[**RestoreDetailed**](RestoreDetailed.md)

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

# **restore_website**
> restore_website(org_id, website_id, backup_id, backup_restore_options=backup_restore_options)

Restore website from a backup

Restores the website's home directory and MySQL databases, and optionally the website's email mailboxes if the `includeEmails` query parameter is set to true. Note that if the website was deleted or any of its entities was deleted through `orchd` (via one or more of the DELETE endpoints), this endpoint does not restore those resources. It may only be used when e.g. one wants to restore the previous state of the mailbox of an existing account (but not a deleted account), or the state of an existing website's home directory. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.backup_restore_options import BackupRestoreOptions
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
    api_instance = openapi_client.BackupsApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    backup_id = 56 # int | The id of the backup.
    backup_restore_options = openapi_client.BackupRestoreOptions() # BackupRestoreOptions | The options used to define what will be restored from the backup snapshot. (optional)

    try:
        # Restore website from a backup
        api_instance.restore_website(org_id, website_id, backup_id, backup_restore_options=backup_restore_options)
    except Exception as e:
        print("Exception when calling BackupsApi->restore_website: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **backup_id** | **int**| The id of the backup. | 
 **backup_restore_options** | [**BackupRestoreOptions**](BackupRestoreOptions.md)| The options used to define what will be restored from the backup snapshot. | [optional] 

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
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

