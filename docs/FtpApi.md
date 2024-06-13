# openapi_client.FtpApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_ftp_user**](FtpApi.md#create_ftp_user) | **POST** /orgs/{org_id}/websites/{website_id}/ftp/users | Creates a new FTP user for a given website
[**delete_ftp_user**](FtpApi.md#delete_ftp_user) | **DELETE** /orgs/{org_id}/websites/{website_id}/ftp/users/{user_id} | Deletes given FTP user
[**get_ftp_users**](FtpApi.md#get_ftp_users) | **GET** /orgs/{org_id}/websites/{website_id}/ftp/users | Returns all ftp users data for a given website
[**update_ftp_user**](FtpApi.md#update_ftp_user) | **PATCH** /orgs/{org_id}/websites/{website_id}/ftp/users/{user_id} | Update given FTP user


# **create_ftp_user**
> NewResourceUuid create_ftp_user(org_id, website_id, new_ftp_user, create_home=create_home)

Creates a new FTP user for a given website

Endpoint for creating a new FTP user. NOTE: user.account well get appended with website's primary domain. i.e. `username` will become `username@domain.com` Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.new_ftp_user import NewFtpUser
from openapi_client.models.new_resource_uuid import NewResourceUuid
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
    api_instance = openapi_client.FtpApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    new_ftp_user = openapi_client.NewFtpUser() # NewFtpUser | FTP User
    create_home = True # bool | If set to true we will try to crete a new home_dir for the user if does not exist. (optional)

    try:
        # Creates a new FTP user for a given website
        api_response = api_instance.create_ftp_user(org_id, website_id, new_ftp_user, create_home=create_home)
        print("The response of FtpApi->create_ftp_user:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FtpApi->create_ftp_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **new_ftp_user** | [**NewFtpUser**](NewFtpUser.md)| FTP User | 
 **create_home** | **bool**| If set to true we will try to crete a new home_dir for the user if does not exist. | [optional] 

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
**201** | FTP user successfully created |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |
**409** | Already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_ftp_user**
> delete_ftp_user(org_id, website_id, user_id, delete_home=delete_home)

Deletes given FTP user

Endpoint for deleting FTP user for a given website. User homeDir can only be deleted if it is a subdir for the website home. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

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
    api_instance = openapi_client.FtpApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    user_id = 'user_id_example' # str | The id of an FTP user.
    delete_home = True # bool | If set to true we will try to delete the homeDir for the user. User homeDir can only be deleted if it is a subdir for the website home. (optional)

    try:
        # Deletes given FTP user
        api_instance.delete_ftp_user(org_id, website_id, user_id, delete_home=delete_home)
    except Exception as e:
        print("Exception when calling FtpApi->delete_ftp_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **user_id** | **str**| The id of an FTP user. | 
 **delete_home** | **bool**| If set to true we will try to delete the homeDir for the user. User homeDir can only be deleted if it is a subdir for the website home. | [optional] 

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
**204** | FTP user successfully deleted |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_ftp_users**
> FtpUsersFullListing get_ftp_users(org_id, website_id)

Returns all ftp users data for a given website

Endpoint for retreaving ftp users for a given website Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.ftp_users_full_listing import FtpUsersFullListing
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
    api_instance = openapi_client.FtpApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Returns all ftp users data for a given website
        api_response = api_instance.get_ftp_users(org_id, website_id)
        print("The response of FtpApi->get_ftp_users:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FtpApi->get_ftp_users: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 

### Return type

[**FtpUsersFullListing**](FtpUsersFullListing.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Ftp Users |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_ftp_user**
> update_ftp_user(org_id, website_id, user_id, ftp_user_update)

Update given FTP user

Endpoint for updating FTP user for a given website We only allow user's homeDir and password to be updated. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.ftp_user_update import FtpUserUpdate
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
    api_instance = openapi_client.FtpApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    user_id = 'user_id_example' # str | The id of an FTP user.
    ftp_user_update = openapi_client.FtpUserUpdate() # FtpUserUpdate | FTP User

    try:
        # Update given FTP user
        api_instance.update_ftp_user(org_id, website_id, user_id, ftp_user_update)
    except Exception as e:
        print("Exception when calling FtpApi->update_ftp_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **user_id** | **str**| The id of an FTP user. | 
 **ftp_user_update** | [**FtpUserUpdate**](FtpUserUpdate.md)| FTP User | 

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
**204** | FTP user successfully updated |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

