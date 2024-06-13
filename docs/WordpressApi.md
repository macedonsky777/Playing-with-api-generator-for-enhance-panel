# openapi_client.WordpressApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**activate_wordpress_theme**](WordpressApi.md#activate_wordpress_theme) | **POST** /orgs/{org_id}/websites/{website_id}/apps/{app_id}/wordpress/themes/{theme}/activate | Activate a WordPress theme
[**create_wordpress_user**](WordpressApi.md#create_wordpress_user) | **POST** /orgs/{org_id}/websites/{website_id}/apps/{app_id}/wordpress/users | Create website WordPress user
[**delete_wordpress_plugin**](WordpressApi.md#delete_wordpress_plugin) | **DELETE** /orgs/{org_id}/websites/{website_id}/apps/{app_id}/wordpress/plugins/{plugin} | Delete website WordPress plugin
[**delete_wordpress_theme**](WordpressApi.md#delete_wordpress_theme) | **DELETE** /orgs/{org_id}/websites/{website_id}/apps/{app_id}/wordpress/themes/{theme} | Delete a WordPress theme
[**delete_wordpress_user**](WordpressApi.md#delete_wordpress_user) | **DELETE** /orgs/{org_id}/websites/{website_id}/apps/{app_id}/wordpress/users/{user_id} | Delete WordPress user
[**get_default_wp_sso_user**](WordpressApi.md#get_default_wp_sso_user) | **GET** /orgs/{org_id}/websites/{website_id}/apps/{app_id}/wordpress/users/default | 
[**get_word_press_maintenance_mode**](WordpressApi.md#get_word_press_maintenance_mode) | **GET** /v2/apps/{app_id}/wordpress/maintenance-mode | Gets the MaintenanceMode for a WordPress installation
[**get_word_press_siteurl**](WordpressApi.md#get_word_press_siteurl) | **GET** /v2/apps/{app_id}/wordpress/url | Fetches the site URL for a WordPress installation
[**get_wordpress_app_version**](WordpressApi.md#get_wordpress_app_version) | **GET** /orgs/{org_id}/websites/{website_id}/apps/{app_id}/wordpress/version | Get WordPress version
[**get_wordpress_config**](WordpressApi.md#get_wordpress_config) | **GET** /orgs/{org_id}/websites/{website_id}/apps/{app_id}/wordpress/wp-config/{wp_option} | Get the WP config value for a given option
[**get_wordpress_installations**](WordpressApi.md#get_wordpress_installations) | **GET** /orgs/{org_id}/websites/{website_id}/apps/wordpress | Trigger discovery of WP installations
[**get_wordpress_latest_version**](WordpressApi.md#get_wordpress_latest_version) | **GET** /utils/wordpress/latest | Get WordPress latest available version
[**get_wordpress_plugins**](WordpressApi.md#get_wordpress_plugins) | **GET** /orgs/{org_id}/websites/{website_id}/apps/{app_id}/wordpress/plugins | Get website WordPress plugins
[**get_wordpress_settings**](WordpressApi.md#get_wordpress_settings) | **GET** /orgs/{org_id}/websites/{website_id}/apps/{app_id}/wordpress | Get Wordpress application settings
[**get_wordpress_themes**](WordpressApi.md#get_wordpress_themes) | **GET** /orgs/{org_id}/websites/{website_id}/apps/{app_id}/wordpress/themes | Get website WordPress themes
[**get_wordpress_user_sso_url**](WordpressApi.md#get_wordpress_user_sso_url) | **GET** /orgs/{org_id}/websites/{website_id}/apps/{app_id}/wordpress/users/{user_id}/sso | Get SSO URL for a WP user
[**get_wordpress_users**](WordpressApi.md#get_wordpress_users) | **GET** /orgs/{org_id}/websites/{website_id}/apps/{app_id}/wordpress/users | 
[**install_wordpress_plugin**](WordpressApi.md#install_wordpress_plugin) | **POST** /orgs/{org_id}/websites/{website_id}/apps/{app_id}/wordpress/plugins | Install a plugin
[**install_wordpress_theme**](WordpressApi.md#install_wordpress_theme) | **POST** /orgs/{org_id}/websites/{website_id}/apps/{app_id}/wordpress/themes | Install a WordPress theme
[**set_default_wp_sso_user**](WordpressApi.md#set_default_wp_sso_user) | **PUT** /orgs/{org_id}/websites/{website_id}/apps/{app_id}/wordpress/users/default | Set WP user as the default SSO user for that website.
[**set_word_press_maintenance_mode**](WordpressApi.md#set_word_press_maintenance_mode) | **PUT** /v2/apps/{app_id}/wordpress/maintenance-mode | Sets the MaintenanceMode for a WordPress installation
[**set_word_press_siteurl**](WordpressApi.md#set_word_press_siteurl) | **PUT** /v2/apps/{app_id}/wordpress/url | Sets the site URL for a WordPress installation
[**set_wordpress_config**](WordpressApi.md#set_wordpress_config) | **PUT** /orgs/{org_id}/websites/{website_id}/apps/{app_id}/wordpress/wp-config | Set a single value of a wp-config.php entry.
[**set_wordpress_theme_auto_update_status**](WordpressApi.md#set_wordpress_theme_auto_update_status) | **PATCH** /orgs/{org_id}/websites/{website_id}/apps/{app_id}/wordpress/themes/{theme}/auto_update | Set WordPress theme auto-update status
[**update_wordpress_app_version**](WordpressApi.md#update_wordpress_app_version) | **PATCH** /orgs/{org_id}/websites/{website_id}/apps/{app_id}/wordpress/version | Update website WP app to specific version or latest
[**update_wordpress_plugin_settings**](WordpressApi.md#update_wordpress_plugin_settings) | **PATCH** /orgs/{org_id}/websites/{website_id}/apps/{app_id}/wordpress/plugins/{plugin} | Updates website WordPress plugin settings
[**update_wordpress_plugin_to_latest**](WordpressApi.md#update_wordpress_plugin_to_latest) | **PATCH** /orgs/{org_id}/websites/{website_id}/apps/{app_id}/wordpress/plugins/{plugin}/version | Updates website WordPress plugin to latest version
[**update_wordpress_settings**](WordpressApi.md#update_wordpress_settings) | **PATCH** /orgs/{org_id}/websites/{website_id}/apps/{app_id}/wordpress | Update Wordpress app settings
[**update_wordpress_theme**](WordpressApi.md#update_wordpress_theme) | **POST** /orgs/{org_id}/websites/{website_id}/apps/{app_id}/wordpress/themes/{theme}/update | Update a WordPress theme
[**update_wordpress_user**](WordpressApi.md#update_wordpress_user) | **PATCH** /orgs/{org_id}/websites/{website_id}/apps/{app_id}/wordpress/users/{user_id} | Update WordPress user


# **activate_wordpress_theme**
> activate_wordpress_theme(org_id, website_id, app_id, theme)

Activate a WordPress theme

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
    api_instance = openapi_client.WordpressApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    app_id = 'app_id_example' # str | The id of the app.
    theme = 'theme_example' # str | The name of the wordpress theme (not file name!).

    try:
        # Activate a WordPress theme
        api_instance.activate_wordpress_theme(org_id, website_id, app_id, theme)
    except Exception as e:
        print("Exception when calling WordpressApi->activate_wordpress_theme: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **app_id** | **str**| The id of the app. | 
 **theme** | **str**| The name of the wordpress theme (not file name!). | 

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
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_wordpress_user**
> create_wordpress_user(org_id, website_id, app_id, new_wp_user)

Create website WordPress user

Creates a new user in this wordpress app. The created user is independent from Enhance logins--it only concerns the wordpress app (which much like Enhance is its own webapp). Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.new_wp_user import NewWpUser
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
    api_instance = openapi_client.WordpressApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    app_id = 'app_id_example' # str | The id of the app.
    new_wp_user = openapi_client.NewWpUser() # NewWpUser | 

    try:
        # Create website WordPress user
        api_instance.create_wordpress_user(org_id, website_id, app_id, new_wp_user)
    except Exception as e:
        print("Exception when calling WordpressApi->create_wordpress_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **app_id** | **str**| The id of the app. | 
 **new_wp_user** | [**NewWpUser**](NewWpUser.md)|  | 

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
**201** | Successful |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_wordpress_plugin**
> delete_wordpress_plugin(org_id, website_id, app_id, plugin)

Delete website WordPress plugin

Deletes the specified wordpress plugin. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

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
    api_instance = openapi_client.WordpressApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    app_id = 'app_id_example' # str | The id of the app.
    plugin = 'plugin_example' # str | The name of the wordpress plugin (not file name!).

    try:
        # Delete website WordPress plugin
        api_instance.delete_wordpress_plugin(org_id, website_id, app_id, plugin)
    except Exception as e:
        print("Exception when calling WordpressApi->delete_wordpress_plugin: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **app_id** | **str**| The id of the app. | 
 **plugin** | **str**| The name of the wordpress plugin (not file name!). | 

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

# **delete_wordpress_theme**
> delete_wordpress_theme(org_id, website_id, app_id, theme)

Delete a WordPress theme

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
    api_instance = openapi_client.WordpressApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    app_id = 'app_id_example' # str | The id of the app.
    theme = 'theme_example' # str | The name of the wordpress theme (not file name!).

    try:
        # Delete a WordPress theme
        api_instance.delete_wordpress_theme(org_id, website_id, app_id, theme)
    except Exception as e:
        print("Exception when calling WordpressApi->delete_wordpress_theme: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **app_id** | **str**| The id of the app. | 
 **theme** | **str**| The name of the wordpress theme (not file name!). | 

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
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_wordpress_user**
> delete_wordpress_user(org_id, website_id, app_id, user_id)

Delete WordPress user

Deletes an existing user in this wordpress app. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

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
    api_instance = openapi_client.WordpressApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    app_id = 'app_id_example' # str | The id of the app.
    user_id = 56 # int | The id of the wordpress user.

    try:
        # Delete WordPress user
        api_instance.delete_wordpress_user(org_id, website_id, app_id, user_id)
    except Exception as e:
        print("Exception when calling WordpressApi->delete_wordpress_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **app_id** | **str**| The id of the app. | 
 **user_id** | **int**| The id of the wordpress user. | 

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

# **get_default_wp_sso_user**
> WpUser get_default_wp_sso_user(org_id, website_id, app_id)



Return previously set default Wordpress SSO user. If WP users exist but none were set to be default, returns 404. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.wp_user import WpUser
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
    api_instance = openapi_client.WordpressApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    app_id = 'app_id_example' # str | The id of the app.

    try:
        api_response = api_instance.get_default_wp_sso_user(org_id, website_id, app_id)
        print("The response of WordpressApi->get_default_wp_sso_user:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WordpressApi->get_default_wp_sso_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **app_id** | **str**| The id of the app. | 

### Return type

[**WpUser**](WpUser.md)

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

# **get_word_press_maintenance_mode**
> MaintenanceModeStatus get_word_press_maintenance_mode(app_id)

Gets the MaintenanceMode for a WordPress installation

### Example


```python
import openapi_client
from openapi_client.models.maintenance_mode_status import MaintenanceModeStatus
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
    api_instance = openapi_client.WordpressApi(api_client)
    app_id = 'app_id_example' # str | The id of the app.

    try:
        # Gets the MaintenanceMode for a WordPress installation
        api_response = api_instance.get_word_press_maintenance_mode(app_id)
        print("The response of WordpressApi->get_word_press_maintenance_mode:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WordpressApi->get_word_press_maintenance_mode: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **app_id** | **str**| The id of the app. | 

### Return type

[**MaintenanceModeStatus**](MaintenanceModeStatus.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successfully returned WordPress MaintenanceMode |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_word_press_siteurl**
> str get_word_press_siteurl(app_id)

Fetches the site URL for a WordPress installation

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
    api_instance = openapi_client.WordpressApi(api_client)
    app_id = 'app_id_example' # str | The id of the app.

    try:
        # Fetches the site URL for a WordPress installation
        api_response = api_instance.get_word_press_siteurl(app_id)
        print("The response of WordpressApi->get_word_press_siteurl:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WordpressApi->get_word_press_siteurl: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **app_id** | **str**| The id of the app. | 

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
**200** | Successfully fetched site url |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_wordpress_app_version**
> GetWordpressAppVersion200Response get_wordpress_app_version(org_id, website_id, app_id)

Get WordPress version

Fetches the WordPress version of a running installation in real time.

### Example


```python
import openapi_client
from openapi_client.models.get_wordpress_app_version200_response import GetWordpressAppVersion200Response
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
    api_instance = openapi_client.WordpressApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    app_id = 'app_id_example' # str | The id of the app.

    try:
        # Get WordPress version
        api_response = api_instance.get_wordpress_app_version(org_id, website_id, app_id)
        print("The response of WordpressApi->get_wordpress_app_version:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WordpressApi->get_wordpress_app_version: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **app_id** | **str**| The id of the app. | 

### Return type

[**GetWordpressAppVersion200Response**](GetWordpressAppVersion200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Version successfully queried |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_wordpress_config**
> WordpressConfig get_wordpress_config(org_id, website_id, app_id, wp_option)

Get the WP config value for a given option

Returns the value of a wp-config.php entry.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.wordpress_config import WordpressConfig
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
    api_instance = openapi_client.WordpressApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    app_id = 'app_id_example' # str | The id of the app.
    wp_option = 'wp_option_example' # str | The wordpress config option.

    try:
        # Get the WP config value for a given option
        api_response = api_instance.get_wordpress_config(org_id, website_id, app_id, wp_option)
        print("The response of WordpressApi->get_wordpress_config:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WordpressApi->get_wordpress_config: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **app_id** | **str**| The id of the app. | 
 **wp_option** | **str**| The wordpress config option. | 

### Return type

[**WordpressConfig**](WordpressConfig.md)

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

# **get_wordpress_installations**
> List[WpInstallation] get_wordpress_installations(org_id, website_id)

Trigger discovery of WP installations

WP installations that were made manually (aside from invoking) orchd APIs aren't immediately discovered by orchd. Invoking this endpoint triggers the discovery and adds installation info to the database.

### Example


```python
import openapi_client
from openapi_client.models.wp_installation import WpInstallation
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
    api_instance = openapi_client.WordpressApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.

    try:
        # Trigger discovery of WP installations
        api_response = api_instance.get_wordpress_installations(org_id, website_id)
        print("The response of WordpressApi->get_wordpress_installations:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WordpressApi->get_wordpress_installations: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 

### Return type

[**List[WpInstallation]**](WpInstallation.md)

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

# **get_wordpress_latest_version**
> WpLatestVersion get_wordpress_latest_version()

Get WordPress latest available version

Returns the latest available WordPress version as published by the WordPress APIs.

### Example


```python
import openapi_client
from openapi_client.models.wp_latest_version import WpLatestVersion
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
    api_instance = openapi_client.WordpressApi(api_client)

    try:
        # Get WordPress latest available version
        api_response = api_instance.get_wordpress_latest_version()
        print("The response of WordpressApi->get_wordpress_latest_version:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WordpressApi->get_wordpress_latest_version: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**WpLatestVersion**](WpLatestVersion.md)

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

# **get_wordpress_plugins**
> WpPluginsFullListing get_wordpress_plugins(org_id, website_id, app_id, refresh_cache=refresh_cache)

Get website WordPress plugins

Returns the plugins installed on wordpress. This is a separate endpoint as it is takes longer to return than the rest of the application endpoints. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.wp_plugins_full_listing import WpPluginsFullListing
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
    api_instance = openapi_client.WordpressApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    app_id = 'app_id_example' # str | The id of the app.
    refresh_cache = True # bool | If set to true, it will bypass internal caching. (optional)

    try:
        # Get website WordPress plugins
        api_response = api_instance.get_wordpress_plugins(org_id, website_id, app_id, refresh_cache=refresh_cache)
        print("The response of WordpressApi->get_wordpress_plugins:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WordpressApi->get_wordpress_plugins: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **app_id** | **str**| The id of the app. | 
 **refresh_cache** | **bool**| If set to true, it will bypass internal caching. | [optional] 

### Return type

[**WpPluginsFullListing**](WpPluginsFullListing.md)

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

# **get_wordpress_settings**
> WpSettings get_wordpress_settings(org_id, website_id, app_id)

Get Wordpress application settings

Queries an existing Wordpress application's settings. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.wp_settings import WpSettings
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
    api_instance = openapi_client.WordpressApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    app_id = 'app_id_example' # str | The id of the app.

    try:
        # Get Wordpress application settings
        api_response = api_instance.get_wordpress_settings(org_id, website_id, app_id)
        print("The response of WordpressApi->get_wordpress_settings:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WordpressApi->get_wordpress_settings: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **app_id** | **str**| The id of the app. | 

### Return type

[**WpSettings**](WpSettings.md)

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

# **get_wordpress_themes**
> WpThemesFullListing get_wordpress_themes(org_id, website_id, app_id, refresh_cache=refresh_cache)

Get website WordPress themes

Returns the themes installed on website's WordPress. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.wp_themes_full_listing import WpThemesFullListing
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
    api_instance = openapi_client.WordpressApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    app_id = 'app_id_example' # str | The id of the app.
    refresh_cache = True # bool | If set to true, it will bypass internal caching. (optional)

    try:
        # Get website WordPress themes
        api_response = api_instance.get_wordpress_themes(org_id, website_id, app_id, refresh_cache=refresh_cache)
        print("The response of WordpressApi->get_wordpress_themes:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WordpressApi->get_wordpress_themes: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **app_id** | **str**| The id of the app. | 
 **refresh_cache** | **bool**| If set to true, it will bypass internal caching. | [optional] 

### Return type

[**WpThemesFullListing**](WpThemesFullListing.md)

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

# **get_wordpress_user_sso_url**
> str get_wordpress_user_sso_url(org_id, website_id, app_id, user_id, should_redirect=should_redirect)

Get SSO URL for a WP user

Session holder must have write access to the website

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
    api_instance = openapi_client.WordpressApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    app_id = 'app_id_example' # str | The id of the app.
    user_id = 56 # int | The id of the wordpress user.
    should_redirect = True # bool | If set to true, the endpoint will send a 307 redirect to the SSO URL. (optional)

    try:
        # Get SSO URL for a WP user
        api_response = api_instance.get_wordpress_user_sso_url(org_id, website_id, app_id, user_id, should_redirect=should_redirect)
        print("The response of WordpressApi->get_wordpress_user_sso_url:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WordpressApi->get_wordpress_user_sso_url: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **app_id** | **str**| The id of the app. | 
 **user_id** | **int**| The id of the wordpress user. | 
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
**200** | Successful |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_wordpress_users**
> WpUsersFullListing get_wordpress_users(org_id, website_id, app_id)



Returns the users of this wordpress app. This is a separate endpoint as it is takes longer to return than most other endpoints. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.wp_users_full_listing import WpUsersFullListing
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
    api_instance = openapi_client.WordpressApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    app_id = 'app_id_example' # str | The id of the app.

    try:
        api_response = api_instance.get_wordpress_users(org_id, website_id, app_id)
        print("The response of WordpressApi->get_wordpress_users:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WordpressApi->get_wordpress_users: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **app_id** | **str**| The id of the app. | 

### Return type

[**WpUsersFullListing**](WpUsersFullListing.md)

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

# **install_wordpress_plugin**
> install_wordpress_plugin(org_id, website_id, app_id, install_wp_plugin, refresh_cache=refresh_cache)

Install a plugin

Adds a specific plugin to a WordPress installation. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.install_wp_plugin import InstallWpPlugin
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
    api_instance = openapi_client.WordpressApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    app_id = 'app_id_example' # str | The id of the app.
    install_wp_plugin = openapi_client.InstallWpPlugin() # InstallWpPlugin | 
    refresh_cache = True # bool | If set to true, it will bypass internal caching. (optional)

    try:
        # Install a plugin
        api_instance.install_wordpress_plugin(org_id, website_id, app_id, install_wp_plugin, refresh_cache=refresh_cache)
    except Exception as e:
        print("Exception when calling WordpressApi->install_wordpress_plugin: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **app_id** | **str**| The id of the app. | 
 **install_wp_plugin** | [**InstallWpPlugin**](InstallWpPlugin.md)|  | 
 **refresh_cache** | **bool**| If set to true, it will bypass internal caching. | [optional] 

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
**201** | Created |  -  |
**400** | Invalid input |  -  |
**401** | Invalid session |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |
**409** | Already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **install_wordpress_theme**
> install_wordpress_theme(org_id, website_id, app_id, install_wp_theme_request, refresh_cache=refresh_cache)

Install a WordPress theme

### Example


```python
import openapi_client
from openapi_client.models.install_wp_theme_request import InstallWpThemeRequest
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
    api_instance = openapi_client.WordpressApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    app_id = 'app_id_example' # str | The id of the app.
    install_wp_theme_request = openapi_client.InstallWpThemeRequest() # InstallWpThemeRequest | 
    refresh_cache = True # bool | If set to true, it will bypass internal caching. (optional)

    try:
        # Install a WordPress theme
        api_instance.install_wordpress_theme(org_id, website_id, app_id, install_wp_theme_request, refresh_cache=refresh_cache)
    except Exception as e:
        print("Exception when calling WordpressApi->install_wordpress_theme: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **app_id** | **str**| The id of the app. | 
 **install_wp_theme_request** | [**InstallWpThemeRequest**](InstallWpThemeRequest.md)|  | 
 **refresh_cache** | **bool**| If set to true, it will bypass internal caching. | [optional] 

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
**200** | Successful |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_default_wp_sso_user**
> set_default_wp_sso_user(org_id, website_id, app_id, body)

Set WP user as the default SSO user for that website.

Idempotently set WP user as the default SSO user for that website. User needs to exist. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

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
    api_instance = openapi_client.WordpressApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    app_id = 'app_id_example' # str | The id of the app.
    body = 3.4 # float | 

    try:
        # Set WP user as the default SSO user for that website.
        api_instance.set_default_wp_sso_user(org_id, website_id, app_id, body)
    except Exception as e:
        print("Exception when calling WordpressApi->set_default_wp_sso_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **app_id** | **str**| The id of the app. | 
 **body** | **float**|  | 

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
**201** | Successful |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_word_press_maintenance_mode**
> set_word_press_maintenance_mode(app_id, body)

Sets the MaintenanceMode for a WordPress installation

### Example


```python
import openapi_client
from openapi_client.models.maintenance_mode import MaintenanceMode
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
    api_instance = openapi_client.WordpressApi(api_client)
    app_id = 'app_id_example' # str | The id of the app.
    body = 'body_example' # str | 

    try:
        # Sets the MaintenanceMode for a WordPress installation
        api_instance.set_word_press_maintenance_mode(app_id, body)
    except Exception as e:
        print("Exception when calling WordpressApi->set_word_press_maintenance_mode: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **app_id** | **str**| The id of the app. | 
 **body** | **str**|  | 

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
**200** | Successfully updated WordPress MaintenanceMode |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_word_press_siteurl**
> set_word_press_siteurl(app_id, body)

Sets the site URL for a WordPress installation

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
    api_instance = openapi_client.WordpressApi(api_client)
    app_id = 'app_id_example' # str | The id of the app.
    body = 'body_example' # str | 

    try:
        # Sets the site URL for a WordPress installation
        api_instance.set_word_press_siteurl(app_id, body)
    except Exception as e:
        print("Exception when calling WordpressApi->set_word_press_siteurl: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **app_id** | **str**| The id of the app. | 
 **body** | **str**|  | 

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
**200** | Successfully updated WordPress site URL |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_wordpress_config**
> set_wordpress_config(org_id, website_id, app_id, wordpress_config)

Set a single value of a wp-config.php entry.

### Example

* Api Key Authentication (sessionCookie):
* Bearer Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.wordpress_config import WordpressConfig
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
    api_instance = openapi_client.WordpressApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    app_id = 'app_id_example' # str | The id of the app.
    wordpress_config = openapi_client.WordpressConfig() # WordpressConfig | 

    try:
        # Set a single value of a wp-config.php entry.
        api_instance.set_wordpress_config(org_id, website_id, app_id, wordpress_config)
    except Exception as e:
        print("Exception when calling WordpressApi->set_wordpress_config: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **app_id** | **str**| The id of the app. | 
 **wordpress_config** | [**WordpressConfig**](WordpressConfig.md)|  | 

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

# **set_wordpress_theme_auto_update_status**
> set_wordpress_theme_auto_update_status(org_id, website_id, app_id, theme, body)

Set WordPress theme auto-update status

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
    api_instance = openapi_client.WordpressApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    app_id = 'app_id_example' # str | The id of the app.
    theme = 'theme_example' # str | The name of the wordpress theme (not file name!).
    body = True # bool | 

    try:
        # Set WordPress theme auto-update status
        api_instance.set_wordpress_theme_auto_update_status(org_id, website_id, app_id, theme, body)
    except Exception as e:
        print("Exception when calling WordpressApi->set_wordpress_theme_auto_update_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **app_id** | **str**| The id of the app. | 
 **theme** | **str**| The name of the wordpress theme (not file name!). | 
 **body** | **bool**|  | 

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
**200** | Successful |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_wordpress_app_version**
> update_wordpress_app_version(org_id, website_id, app_id)

Update website WP app to specific version or latest

Updates an existing website Wordpress application's version to given version (defaults to latest). If the installation is already on its latest version, returns 200 without doing any work. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

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
    api_instance = openapi_client.WordpressApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    app_id = 'app_id_example' # str | The id of the app.

    try:
        # Update website WP app to specific version or latest
        api_instance.update_wordpress_app_version(org_id, website_id, app_id)
    except Exception as e:
        print("Exception when calling WordpressApi->update_wordpress_app_version: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **app_id** | **str**| The id of the app. | 

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
**200** | Successfully updated the WP core or there&#39;s no update to apply |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_wordpress_plugin_settings**
> update_wordpress_plugin_settings(org_id, website_id, app_id, plugin, update_wp_plugin)

Updates website WordPress plugin settings

Updates the settings for a WP plugin, such as whether the plugin should be active. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.update_wp_plugin import UpdateWpPlugin
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
    api_instance = openapi_client.WordpressApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    app_id = 'app_id_example' # str | The id of the app.
    plugin = 'plugin_example' # str | The name of the wordpress plugin (not file name!).
    update_wp_plugin = openapi_client.UpdateWpPlugin() # UpdateWpPlugin | 

    try:
        # Updates website WordPress plugin settings
        api_instance.update_wordpress_plugin_settings(org_id, website_id, app_id, plugin, update_wp_plugin)
    except Exception as e:
        print("Exception when calling WordpressApi->update_wordpress_plugin_settings: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **app_id** | **str**| The id of the app. | 
 **plugin** | **str**| The name of the wordpress plugin (not file name!). | 
 **update_wp_plugin** | [**UpdateWpPlugin**](UpdateWpPlugin.md)|  | 

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
**204** | Successful |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_wordpress_plugin_to_latest**
> update_wordpress_plugin_to_latest(org_id, website_id, app_id, plugin)

Updates website WordPress plugin to latest version

Updates the specified wordpress plugin to its latest version. Does nothing if the plugin is already latest. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

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
    api_instance = openapi_client.WordpressApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    app_id = 'app_id_example' # str | The id of the app.
    plugin = 'plugin_example' # str | The name of the wordpress plugin (not file name!).

    try:
        # Updates website WordPress plugin to latest version
        api_instance.update_wordpress_plugin_to_latest(org_id, website_id, app_id, plugin)
    except Exception as e:
        print("Exception when calling WordpressApi->update_wordpress_plugin_to_latest: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **app_id** | **str**| The id of the app. | 
 **plugin** | **str**| The name of the wordpress plugin (not file name!). | 

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

# **update_wordpress_settings**
> update_wordpress_settings(org_id, website_id, app_id, update_wp_settings)

Update Wordpress app settings

Updates an existing website WP application's settings. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.update_wp_settings import UpdateWpSettings
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
    api_instance = openapi_client.WordpressApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    app_id = 'app_id_example' # str | The id of the app.
    update_wp_settings = openapi_client.UpdateWpSettings() # UpdateWpSettings | 

    try:
        # Update Wordpress app settings
        api_instance.update_wordpress_settings(org_id, website_id, app_id, update_wp_settings)
    except Exception as e:
        print("Exception when calling WordpressApi->update_wordpress_settings: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **app_id** | **str**| The id of the app. | 
 **update_wp_settings** | [**UpdateWpSettings**](UpdateWpSettings.md)|  | 

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
**200** | Successful |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges or operation not allowed by plan |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_wordpress_theme**
> update_wordpress_theme(org_id, website_id, app_id, theme)

Update a WordPress theme

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
    api_instance = openapi_client.WordpressApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    app_id = 'app_id_example' # str | The id of the app.
    theme = 'theme_example' # str | The name of the wordpress theme (not file name!).

    try:
        # Update a WordPress theme
        api_instance.update_wordpress_theme(org_id, website_id, app_id, theme)
    except Exception as e:
        print("Exception when calling WordpressApi->update_wordpress_theme: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **app_id** | **str**| The id of the app. | 
 **theme** | **str**| The name of the wordpress theme (not file name!). | 

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
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_wordpress_user**
> update_wordpress_user(org_id, website_id, app_id, user_id, update_wp_user)

Update WordPress user

Updates an existing user in this wordpress app. Session holder must be at least a `SuperAdmin` in this org or a parent org, or be a member in this org that has access to the website.

### Example


```python
import openapi_client
from openapi_client.models.update_wp_user import UpdateWpUser
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
    api_instance = openapi_client.WordpressApi(api_client)
    org_id = 'org_id_example' # str | The id of the organization.
    website_id = 'website_id_example' # str | The id of the website.
    app_id = 'app_id_example' # str | The id of the app.
    user_id = 56 # int | The id of the wordpress user.
    update_wp_user = openapi_client.UpdateWpUser() # UpdateWpUser | 

    try:
        # Update WordPress user
        api_instance.update_wordpress_user(org_id, website_id, app_id, user_id, update_wp_user)
    except Exception as e:
        print("Exception when calling WordpressApi->update_wordpress_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**| The id of the organization. | 
 **website_id** | **str**| The id of the website. | 
 **app_id** | **str**| The id of the app. | 
 **user_id** | **int**| The id of the wordpress user. | 
 **update_wp_user** | [**UpdateWpUser**](UpdateWpUser.md)|  | 

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
**204** | Successful |  -  |
**400** | Invalid input |  -  |
**403** | Insufficient privileges |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

