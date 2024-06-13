# openapi_client.MysqlApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_website_my_sql_user**](MysqlApi.md#create_website_my_sql_user) | **POST** /orgs/{org_id}/websites/{website_id}/mysql-users | Create website MySQL database user
[**create_website_my_sql_user_access_hosts**](MysqlApi.md#create_website_my_sql_user_access_hosts) | **POST** /orgs/{org_id}/websites/{website_id}/mysql-users/{user_id}/access-hosts | Create website MySQL database user access hosts
[**create_website_my_sqldb**](MysqlApi.md#create_website_my_sqldb) | **POST** /orgs/{org_id}/websites/{website_id}/mysql-dbs | Create a MySQL database for website
[**delete_website_my_sql_user**](MysqlApi.md#delete_website_my_sql_user) | **DELETE** /orgs/{org_id}/websites/{website_id}/mysql-users/{user_id} | Delete website MySQL database user
[**delete_website_my_sql_user_access_hosts**](MysqlApi.md#delete_website_my_sql_user_access_hosts) | **DELETE** /orgs/{org_id}/websites/{website_id}/mysql-users/{user_id}/access-hosts | Delete website MySQL database user access hosts
[**delete_website_my_sqldb**](MysqlApi.md#delete_website_my_sqldb) | **DELETE** /orgs/{org_id}/websites/{website_id}/mysql-dbs/{db_id} | Delete website MySQL database
[**download_sql**](MysqlApi.md#download_sql) | **GET** /orgs/{org_id}/websites/{website_id}/mysql-dbs/{db_id}/sql | Takes a backup of given database and returns it gziped
[**get_org_my_sqldbs**](MysqlApi.md#get_org_my_sqldbs) | **GET** /orgs/{org_id}/mysql-dbs | Get org&#39;s MySQL databases
[**get_php_my_admin_sso_url**](MysqlApi.md#get_php_my_admin_sso_url) | **GET** /orgs/{org_id}/websites/{website_id}/mysql-dbs/{db_id}/sso | Get phpMyAdmin SSO URL
[**get_website_my_sql_users**](MysqlApi.md#get_website_my_sql_users) | **GET** /orgs/{org_id}/websites/{website_id}/mysql-users | Get website MySQL database users
[**get_website_my_sqldbs**](MysqlApi.md#get_website_my_sqldbs) | **GET** /orgs/{org_id}/websites/{website_id}/mysql-dbs | Get website MySQL databases
[**set_website_my_sql_user_privileges**](MysqlApi.md#set_website_my_sql_user_privileges) | **PUT** /orgs/{org_id}/websites/{website_id}/mysql-users/{user_id}/privileges | Create website MySQL database user privileges
[**update_website_my_sql_user**](MysqlApi.md#update_website_my_sql_user) | **PUT** /orgs/{org_id}/websites/{website_id}/mysql-users/{user_id} | Update website MySQL database user
[**upload_sql**](MysqlApi.md#upload_sql) | **POST** /v2/mysql/{db_id}/sql | Uploads sql file and executes it against db


# **create_website_my_sql_user**
> NewResourceUuid create_website_my_sql_user(org_id, website_id, new_my_sql_user)

Create website MySQL database user

Creates a new MySQL database user for the given website database. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.new_my_sql_user import NewMySQLUser
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
    api_instance = openapi_client.MysqlApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    new_my_sql_user = openapi_client.NewMySQLUser() # NewMySQLUser | New user details.

    try:
        # Create website MySQL database user
        api_response = api_instance.create_website_my_sql_user(org_id, website_id, new_my_sql_user)
        print("The response of MysqlApi->create_website_my_sql_user:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MysqlApi->create_website_my_sql_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **new_my_sql_user** | [**NewMySQLUser**](NewMySQLUser.md)| New user details. | 

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
**201** | Database user successfully created |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |
**409** | Already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_website_my_sql_user_access_hosts**
> create_website_my_sql_user_access_hosts(org_id, website_id, db_id, user_id, my_sql_user_access_hosts)

Create website MySQL database user access hosts

Adds for the given user new access hosts to website's MySQL database. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.my_sql_user_access_hosts import MySQLUserAccessHosts
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
    api_instance = openapi_client.MysqlApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    db_id = 'db_id_example' # str | The id of the database.
    user_id = 'user_id_example' # str | The id of the database user.
    my_sql_user_access_hosts = openapi_client.MySQLUserAccessHosts() # MySQLUserAccessHosts | User access hosts.

    try:
        # Create website MySQL database user access hosts
        api_instance.create_website_my_sql_user_access_hosts(org_id, website_id, db_id, user_id, my_sql_user_access_hosts)
    except Exception as e:
        print("Exception when calling MysqlApi->create_website_my_sql_user_access_hosts: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **db_id** | **str**| The id of the database. | 
 **user_id** | **str**| The id of the database user. | 
 **my_sql_user_access_hosts** | [**MySQLUserAccessHosts**](MySQLUserAccessHosts.md)| User access hosts. | 

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
**200** | Database user access hosts successfully updated |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_website_my_sqldb**
> NewResourceUuid create_website_my_sqldb(org_id, website_id, new_my_sqldb)

Create a MySQL database for website

Creates a new MySQL database for the given website. The supplied name must conform to the following regular expression: `^[0-9a-z$_]+$`. That is, a name may only contain alphanumerical characters, dollar signs, and underscores. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.new_my_sqldb import NewMySQLDB
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
    api_instance = openapi_client.MysqlApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    new_my_sqldb = openapi_client.NewMySQLDB() # NewMySQLDB | New database details.

    try:
        # Create a MySQL database for website
        api_response = api_instance.create_website_my_sqldb(org_id, website_id, new_my_sqldb)
        print("The response of MysqlApi->create_website_my_sqldb:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MysqlApi->create_website_my_sqldb: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **new_my_sqldb** | [**NewMySQLDB**](NewMySQLDB.md)| New database details. | 

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
**201** | Database successfully created |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |
**409** | Already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_website_my_sql_user**
> delete_website_my_sql_user(org_id, website_id, user_id)

Delete website MySQL database user

Delete website's MySQL database. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

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
    api_instance = openapi_client.MysqlApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    user_id = 'user_id_example' # str | The id of the database user.

    try:
        # Delete website MySQL database user
        api_instance.delete_website_my_sql_user(org_id, website_id, user_id)
    except Exception as e:
        print("Exception when calling MysqlApi->delete_website_my_sql_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **user_id** | **str**| The id of the database user. | 

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
**204** | Database user successfully deleted |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_website_my_sql_user_access_hosts**
> delete_website_my_sql_user_access_hosts(org_id, website_id, db_id, user_id, my_sql_user_access_hosts)

Delete website MySQL database user access hosts

Removes from the given user access hosts to website's MySQL database. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.my_sql_user_access_hosts import MySQLUserAccessHosts
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
    api_instance = openapi_client.MysqlApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    db_id = 'db_id_example' # str | The id of the database.
    user_id = 'user_id_example' # str | The id of the database user.
    my_sql_user_access_hosts = openapi_client.MySQLUserAccessHosts() # MySQLUserAccessHosts | User access hosts.

    try:
        # Delete website MySQL database user access hosts
        api_instance.delete_website_my_sql_user_access_hosts(org_id, website_id, db_id, user_id, my_sql_user_access_hosts)
    except Exception as e:
        print("Exception when calling MysqlApi->delete_website_my_sql_user_access_hosts: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **db_id** | **str**| The id of the database. | 
 **user_id** | **str**| The id of the database user. | 
 **my_sql_user_access_hosts** | [**MySQLUserAccessHosts**](MySQLUserAccessHosts.md)| User access hosts. | 

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
**204** | Database user access hosts successfully deleted |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_website_my_sqldb**
> delete_website_my_sqldb(org_id, website_id, db_id)

Delete website MySQL database

Delete website's MySQL database. NOTE: All data will be lost after this endpoint returns. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

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
    api_instance = openapi_client.MysqlApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    db_id = 'db_id_example' # str | The id of the database.

    try:
        # Delete website MySQL database
        api_instance.delete_website_my_sqldb(org_id, website_id, db_id)
    except Exception as e:
        print("Exception when calling MysqlApi->delete_website_my_sqldb: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **db_id** | **str**| The id of the database. | 

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
**204** | Database successfully deleted |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **download_sql**
> str download_sql(org_id, website_id, db_id)

Takes a backup of given database and returns it gziped

Performs a database backup into an sql, gzips the sql and returns the file system path for subsequent download with filerd.

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
    api_instance = openapi_client.MysqlApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    db_id = 'db_id_example' # str | The id of the database.

    try:
        # Takes a backup of given database and returns it gziped
        api_response = api_instance.download_sql(org_id, website_id, db_id)
        print("The response of MysqlApi->download_sql:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MysqlApi->download_sql: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **db_id** | **str**| The id of the database. | 

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
**200** | Path to SQL file relative to the website&#39;s home dir |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_org_my_sqldbs**
> MySQLDBsListing get_org_my_sqldbs(org_id, offset=offset, limit=limit, sort_by=sort_by, sort_order=sort_order, search=search)

Get org's MySQL databases

Returns all MySQL databases belonging to the given organization. The results may optionally be filtered. Session holder must be at least a `SuperAdmin` in this org or a parent org.

### Example


```python
import openapi_client
from openapi_client.models.my_sqldbs_listing import MySQLDBsListing
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
    api_instance = openapi_client.MysqlApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    offset = 56 # int | The offset from which to return items. (optional)
    limit = 56 # int | The maximum number of items to return. (optional)
    sort_by = 'sort_by_example' # str | The field by which to sort. (optional)
    sort_order = 'sort_order_example' # str | The direction in which to sort. Possible values are 'asc' and 'desc', defaulting to 'asc'. (optional)
    search = 'search_example' # str | Limit the result set to the resources whose names, partially and case insensitively, match the specified search term. E.g. for websites, this is their domain or tag, for databases the database name, for emails the email address or mailbox name, etc. A website will also be returned if the search term exactly matches the website's uuid. (optional)

    try:
        # Get org's MySQL databases
        api_response = api_instance.get_org_my_sqldbs(org_id, offset=offset, limit=limit, sort_by=sort_by, sort_order=sort_order, search=search)
        print("The response of MysqlApi->get_org_my_sqldbs:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MysqlApi->get_org_my_sqldbs: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **offset** | **int**| The offset from which to return items. | [optional] 
 **limit** | **int**| The maximum number of items to return. | [optional] 
 **sort_by** | **str**| The field by which to sort. | [optional] 
 **sort_order** | **str**| The direction in which to sort. Possible values are &#39;asc&#39; and &#39;desc&#39;, defaulting to &#39;asc&#39;. | [optional] 
 **search** | **str**| Limit the result set to the resources whose names, partially and case insensitively, match the specified search term. E.g. for websites, this is their domain or tag, for databases the database name, for emails the email address or mailbox name, etc. A website will also be returned if the search term exactly matches the website&#39;s uuid. | [optional] 

### Return type

[**MySQLDBsListing**](MySQLDBsListing.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Databases successfully queried |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_php_my_admin_sso_url**
> str get_php_my_admin_sso_url(org_id, website_id, db_id, should_redirect=should_redirect)

Get phpMyAdmin SSO URL

Fetches a single sign-on URL to access phpMyAdmin for this database without the need to log in.

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
    api_instance = openapi_client.MysqlApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    db_id = 'db_id_example' # str | The id of the database.
    should_redirect = True # bool | If set to true, the endpoint will send a 307 redirect to the SSO URL. (optional)

    try:
        # Get phpMyAdmin SSO URL
        api_response = api_instance.get_php_my_admin_sso_url(org_id, website_id, db_id, should_redirect=should_redirect)
        print("The response of MysqlApi->get_php_my_admin_sso_url:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MysqlApi->get_php_my_admin_sso_url: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **db_id** | **str**| The id of the database. | 
 **should_redirect** | **bool**| If set to true, the endpoint will send a 307 redirect to the SSO URL. | [optional] 

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
**200** | SSO URL Fetched |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_my_sql_users**
> MySQLUsersFullListing get_website_my_sql_users(org_id, website_id)

Get website MySQL database users

Returns all MySQL users belonging to the given website database. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.my_sql_users_full_listing import MySQLUsersFullListing
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
    api_instance = openapi_client.MysqlApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Get website MySQL database users
        api_response = api_instance.get_website_my_sql_users(org_id, website_id)
        print("The response of MysqlApi->get_website_my_sql_users:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MysqlApi->get_website_my_sql_users: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 

### Return type

[**MySQLUsersFullListing**](MySQLUsersFullListing.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Database users successfully queried |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website_my_sqldbs**
> MySQLDBsFullListing get_website_my_sqldbs(org_id, website_id)

Get website MySQL databases

Returns all MySQL databases belonging to the given website. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.my_sqldbs_full_listing import MySQLDBsFullListing
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
    api_instance = openapi_client.MysqlApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Get website MySQL databases
        api_response = api_instance.get_website_my_sqldbs(org_id, website_id)
        print("The response of MysqlApi->get_website_my_sqldbs:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MysqlApi->get_website_my_sqldbs: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 

### Return type

[**MySQLDBsFullListing**](MySQLDBsFullListing.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Databases successfully queried |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_website_my_sql_user_privileges**
> set_website_my_sql_user_privileges(org_id, website_id, user_id, my_sql_user_grants)

Create website MySQL database user privileges

Sets the privileges for a user on a given MySQL database.  This will override their current privileges. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.my_sql_user_grants import MySQLUserGrants
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
    api_instance = openapi_client.MysqlApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    user_id = 'user_id_example' # str | The id of the database user.
    my_sql_user_grants = openapi_client.MySQLUserGrants() # MySQLUserGrants | User privilege grants.

    try:
        # Create website MySQL database user privileges
        api_instance.set_website_my_sql_user_privileges(org_id, website_id, user_id, my_sql_user_grants)
    except Exception as e:
        print("Exception when calling MysqlApi->set_website_my_sql_user_privileges: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **user_id** | **str**| The id of the database user. | 
 **my_sql_user_grants** | [**MySQLUserGrants**](MySQLUserGrants.md)| User privilege grants. | 

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
**201** | Database user privileges successfully updated |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |
**409** | Already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_website_my_sql_user**
> update_website_my_sql_user(org_id, website_id, user_id, my_sql_user_update)

Update website MySQL database user

Updates website's MySQL database user's password (username update coming later). Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.my_sql_user_update import MySQLUserUpdate
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
    api_instance = openapi_client.MysqlApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    user_id = 'user_id_example' # str | The id of the database user.
    my_sql_user_update = openapi_client.MySQLUserUpdate() # MySQLUserUpdate | User update details.

    try:
        # Update website MySQL database user
        api_instance.update_website_my_sql_user(org_id, website_id, user_id, my_sql_user_update)
    except Exception as e:
        print("Exception when calling MysqlApi->update_website_my_sql_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **user_id** | **str**| The id of the database user. | 
 **my_sql_user_update** | [**MySQLUserUpdate**](MySQLUserUpdate.md)| User update details. | 

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
**200** | Database user successfully updated |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upload_sql**
> upload_sql(db_id, sql, force=force)

Uploads sql file and executes it against db

Uploads an sql file which is then executed against given db. Allowed file types are '.sql', '.gz' and '.zip'. The gzip-ed file must be a valid sql. The zip archive may contain only one '.sql' file, however the file can be within a directory. If the force flag is set to true (default is false), the SQL execution will not stop when an error is raised (corresponds to the --force option of mysql cli). The max allowed size is 500 MB.

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
    api_instance = openapi_client.MysqlApi(api_client)
    db_id = 'db_id_example' # str | The id of the database.
    sql = None # bytearray | Upload either a raw sql file (must be utf8 valid string) or .zip or .gz file with the sql string.
    force = False # bool |  (optional) (default to False)

    try:
        # Uploads sql file and executes it against db
        api_instance.upload_sql(db_id, sql, force=force)
    except Exception as e:
        print("Exception when calling MysqlApi->upload_sql: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **db_id** | **str**| The id of the database. | 
 **sql** | **bytearray**| Upload either a raw sql file (must be utf8 valid string) or .zip or .gz file with the sql string. | 
 **force** | **bool**|  | [optional] [default to False]

### Return type

void (empty response body)

### Authorization

[sessionCookie](../README.md#sessionCookie), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

